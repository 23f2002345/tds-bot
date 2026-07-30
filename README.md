# tds-bot

This is an AI-powered Telegram bot which acts as a data analyst agent that can answer complex data questions by writing and executing Python code on the fly.

##  Bot Details
- **Telegram Username**: @Proj_1234_bot
- **Hosted on**: Railway
- **Core Brain**: LLM (via aipipe.org)

##  Features
- **JSON-Only Replies**: Responds to every message with exactly one valid JSON object.
- **Agentic Data Analysis**: Uses a `run_python` tool to fetch public datasets (like MOSPI) and process them using `pandas` and `numpy`.
- **Public Run Log**: Every interaction is logged to a publicly accessible JSONL file for grading.
- **Multi-turn Context**: Remembers the last 20 messages in a chat to handle follow-up questions.

##  Repository Structure
- `main.py`: The core application (FastAPI web server + Telegram polling thread).
- `requirements.txt`: List of Python dependencies.


##  Technical Architecture
- **Web Framework**: FastAPI handles the `/health` and `/run.jsonl` endpoints.
- **Polling**: Uses a background thread to long-poll the Telegram Bot API.
- **Execution Sandbox**: The agent can run Python code locally to perform calculations or data manipulation.

## Public Log
The required execution log for grading can be found at:
`https://your-railway-url.up.railway.app/run.jsonl`

## Setup & Local Development
1. Clone the repo:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git

