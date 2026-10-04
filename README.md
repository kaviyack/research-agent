# Research Agent

Research Agent is a small command-line AI research assistant built with LangChain and OpenRouter. It accepts a research question, sends it to an OpenRouter-hosted model, and parses the response into a structured format with a topic, summary, sources, and tools used.

## Features

- Uses OpenRouter's OpenAI-compatible API endpoint
- Loads API keys from a local `.env` file
- Uses LangChain prompt templates and output parsing
- Returns responses as a Pydantic `ResearchResponse` object

## Project Structure

```text
.
├── main.py
├── requirements.txt
├── tools.py
├── .env
└── README.md
```

## Setup

Create and activate a virtual environment:

```powershell
python -m venv venv
.\venv\Scripts\activate
```

Install dependencies:

```powershell
pip install -r requirements.txt
```

Create a `.env` file in the project root:

```env
OPENROUTER_API_KEY="your_openrouter_api_key_here"
```

## Usage

Run the app:

```powershell
python .\main.py
```

Then enter a topic or question when prompted:

```text
What can I help you research?
```

## Notes

- Do not commit your `.env` file.
- `tools.py` is currently reserved for future research tools such as web search, Wikipedia lookup, or file saving.
