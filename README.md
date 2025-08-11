# Web-Scraping-AI-Agent
FastAPI Multi-Agent Web Scraper with Azure OpenAI
This project is a FastAPI-based multi-agent system that uses Azure OpenAI + LangChain to handle intelligent tasks like web scraping, profile retrieval, and email drafting. The core functionality is a web scraper tool built with BeautifulSoup, integrated into a LangChain Zero-Shot Agent that can use multiple tools dynamically based on natural language queries.

Features
Multi-Agent Architecture with LangChain tools

Azure OpenAI Integration for natural language reasoning

BeautifulSoup Web Scraper for headlines & content extraction

Politeness Delay to avoid overloading servers

Extendable Tooling — easily add more agents for different tasks

FastAPI REST Endpoint for easy integration with other services

Tech Stack
Python 3.9+

FastAPI — for serving API requests

LangChain — for agent orchestration

Azure OpenAI — for LLM reasoning

BeautifulSoup4 — for HTML parsing

Requests — for HTTP requests

Installation
# 1️⃣ Clone the repository
git clone https://github.com/yourusername/fastapi-multiagent-scraper.git
cd fastapi-multiagent-scraper

# 2️⃣ Create a virtual environment
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 3️⃣ Install dependencies
pip install -r requirements.txt

Environment Variables
Edit the script and set your Azure OpenAI credentials:
AZURE_OPENAI_KEY = "your-azure-api-key"
AZURE_OPENAI_ENDPOINT = "https://your-resource.openai.azure.com/"
DEPLOYMENT_NAME = "your-deployment-name"

Running the API
uvicorn main:app --reload
The API will be available at: http://127.0.0.1:8000

API Usage
POST /agent
{
  "query": "scrape https://example.com for all headlines"
}
Response
{
  "result": "- Headline 1\n- Headline 2\n- Headline 3"
}

