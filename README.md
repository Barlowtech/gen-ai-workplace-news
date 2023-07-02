# gen-ai-workplace-news
This Python application serves as a news article scraper, summarizer, and speech synthesizer, specifically focusing on articles related to the use of generative AI in the workplace.

Here's a detailed breakdown of what each section does:

**API Key Configuration:**
The program begins by loading API keys for the OpenAI API, the News API, and the Google Drive API from a secure config.json file. This is done to avoid hardcoding sensitive data in the script.

**News Article Scraping:**
The script then sends a request to the News API to fetch the top 10 recent news articles (from the last 5 days) that are related to the use of generative AI in the workplace. For each article retrieved, it uses the BeautifulSoup library to scrape the full text of the article.

**Article Summarization:**
The full text of each article is then passed to the OpenAI API, which uses the GPT-4 model to generate a summary of the article. This is done within a function that includes a specific prompt for the AI, instructing it to act as an employee researcher and to focus the summary on components related to how AI could be used by employees or in the workplace.

**Speech Synthesis:**
The script then combines all the summaries into a single string and uses the Google Text-to-Speech library (gTTS) to convert this text into an MP3 audio file.

**Word Document Creation:**
In parallel with the speech synthesis, the script also creates a Word document using the docx library. This document contains the summaries as well as hyperlinks to the original articles.

**Google Drive Upload:**
Lastly, the script uploads both the MP3 audio file and the Word document to Google Drive using the PyDrive library. This allows the files to be easily accessed from anywhere.

Overall, this application is a comprehensive tool for gathering, summarizing, and presenting information about the use of generative AI in the workplace, making it easier to stay updated on recent developments in this field.
