# Neon AI - Flask GPT Chatbot

A simple Flask application that serves a chatbot using OpenAI’s GPT-3.5-turbo API, with fallback local responses.

## Features

Chat endpoint (/chat) using GPT-3.5-turbo.

Local response library when API errors occur.

Error handling for authentication, rate limits, connection issues, and general API errors.

CORS enabled for cross-origin requests.

Environment configuration via .env and python-dotenv.

Detailed logging of requests and processing times.

## Prerequisites

Python 3.8+

OpenAI API key

## Installation

Clone the repo:

git clone <repo-url>  
cd <repo-directory>  

## Install dependencies:

pip install -r requirements.txt  

## Create a .env file in the project root:

OPENAI_API_KEY=your_api_key_here

## Usage

python app.py  

The app runs on http://0.0.0.0:5000.

Send POST requests to /chat with JSON {"message": "Your text"} to get a reply.

<img width="1853" height="961" alt="image" src="https://github.com/user-attachments/assets/3e07e855-c715-4eef-95f8-6578f49ed47b" />


## Project Structure
text
├── app.py            # Main Flask application  
├── requirements.txt  # Python dependencies  
├── .env              # Environment variables (not committed)  
└── templates/  
    └── index.html    # Basic chat UI  

## Error Handling

AuthenticationError: Falls back to local response.

RateLimitError: Uses local response if API limit is reached.

APIConnectionError: Uses local response on connection issues.

APIError & Exceptions: Logs errors and falls back locally.
