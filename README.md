# RAEF.AI: Reverse Fear Score for Cryptocurrency Sentiment Analysis

## Table of Contents
1. [Overview](#overview)
2. [Key Features](#key-features)
3. [Technology Stack](#technology-stack)
4. [Setup Instructions](#setup-instructions)
5. [Usage](#usage)
6. [Contributing](#contributing)
7. [License](#license)
8. [Acknowledgments](#acknowledgments)

---

## Overview

RAEF.AI is an advanced AI-driven platform designed to calculate the **Reverse Fear Score (RFS)** for cryptocurrencies. The RFS leverages sentiment analysis from Twitter, Reddit, and NewsAPI, combined with volatility and historical recovery data, to identify hidden opportunities in the market. Whether you're a seasoned trader or just starting out, RAEF.AI helps you make smarter, data-backed decisions by turning fear into profit.

The project includes:
- A Telegram bot (`raef_ai_bot.py`) for real-time sentiment analysis.
- A futuristic web interface for visualizing RFS and other analytics.
- A robust backend API built with FastAPI and Python for serving RFS data.

---

## Key Features

- **Reverse Fear Score (RFS)**: Predicts market reversals using sentiment, volatility, and historical recovery data.
- **Multi-Source Sentiment Analysis**: Analyzes sentiment from Twitter, Reddit, and NewsAPI.
- **Telegram Bot Integration**: Provides instant access to RFS and sentiment data via Telegram commands.
- **Futuristic Web Interface**: Offers a sleek, modern dashboard for traders to visualize sentiment trends.
- **Volatility Modeling**: Incorporates CoinGecko's 7-day price volatility data for more accurate predictions.
- **Historical Recovery Insights**: Uses hardcoded recovery scores for top cryptocurrencies (e.g., Bitcoin, Ethereum).
- **Scalable Architecture**: Modular design allows for easy integration of additional data sources and features.

---

## Technology Stack

- **Backend**: Python, FastAPI, Uvicorn, Twikit (Twitter scraping), Async PRAW (Reddit scraping), VaderSentiment, CoinGecko API, NewsAPI.
- **Frontend**: React.js, Vite, Tailwind CSS, Recharts (for visualizations), Framer Motion (for animations).
- **Database**: Redis (for caching sentiment and RFS data).
- **Telegram Bot**: Python-Telegram-Bot library for handling user interactions.

---

## Setup Instructions

### Prerequisites
- Python 3.10+ installed on your system.
- Node.js and npm/yarn installed for frontend development.
- A valid `.env` file with API keys and credentials.

### Backend Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/raef.ai.git
   cd raef.ai/Backend

2. Install dependencies: 
bash
 
 
1
pip install -r requirements.txt
 
 

Set up environment variables:
Create a .env file in the Backend directory with the following keys: 
plaintext
 
NEWS_API_KEY=your_news_api_key
REDDIT_CLIENT_ID=your_reddit_client_id
REDDIT_CLIENT_SECRET=your_reddit_client_secret
REDDIT_USER_AGENT=your_user_agent
COINGECKO_API_URL=https://api.coingecko.com/api/v3
TWITTER_COOKIES_PATH=./cookies.json
TELEGRAM_BOT_TOKEN=your_telegram_bot_token
 
 

Start the backend server: 
bash
 

     
    
    uvicorn main:app --reload
     
     
     

Frontend Setup 

    Navigate to the frontend directory: 
    bash
     

 
1
cd raef.ai/Frontend
 
 

Install dependencies: 
bash
 
 
1
npm install
 
 

Start the development server: 
bash
 

     
    1
    npm run dev
     
     
     

Telegram Bot Setup 

    Ensure the Telegram bot token is set in the .env file. 

    Run the bot script: 
    bash
     

     
    1
    python raef_ai_bot.py
     
     

    Test the bot in Telegram: 
        /start: Start the bot.
        /mood <coin>: Get sentiment analysis for a cryptocurrency.
        /rfs <coin>: Calculate the Reverse Fear Score for a cryptocurrency.
        /help: View available commands.
         
     

Usage 
Telegram Bot Commands 

    /start: Initializes the bot and provides a welcome message.
    /price: Fetches the current price of $RAEF tokens.
    /mood <coin>: Displays sentiment analysis for the specified cryptocurrency across multiple sources (Twitter, Reddit, News).
    /rfs <coin>: Calculates and displays the Reverse Fear Score for the specified cryptocurrency.
    /help: Lists all available commands.
     

Web Interface 

    Open the website at http://localhost:5173 (or your deployed URL).
    Use the search bar to explore RFS and sentiment data for any cryptocurrency.
    Navigate through the dashboard to view detailed charts, market trends, and historical insights.
     

Example Output 

For the command /rfs bitcoin, the bot returns: 
 
 

1. 🛡️ Reverse Fear Score for Bitcoin:
2. Market Data:
3. Price: $29,875.42
4. Market Cap: $598B
5. 24h Change: +2.4%
6. Score: 65.79%
7. Interpretation: Bullish
 
 
Contributing 

We welcome contributions from the community! To contribute: 

    Fork the repository.
    Create a new branch for your feature or bug fix:
    bash
     

 

git checkout -b feature/new-feature
 
 
Commit your changes:
bash
 

     
  
    git commit -m "Add new feature"
     
     
    Push to your fork and submit a pull request.
     

Please ensure your code adheres to the existing style guidelines and includes tests where applicable. 
License 

This project is licensed under the MIT License —see the LICENSE  file for details. 
Acknowledgments 

    VaderSentiment : For sentiment analysis of text data.
    CoinGecko API : For providing market data and volatility metrics.
    NewsAPI : For fetching real-time news articles about cryptocurrencies.
    Async PRAW : For analyzing sentiment from Reddit posts.
    Twikit : For reliable Twitter scraping without requiring API keys.
    Python-Telegram-Bot : For building and deploying the Telegram bot.
    React/Vite : For creating a fast, responsive web interface.
    Recharts : For visualizing sentiment and RFS data.
     

Contact 

For questions, feedback, or collaboration opportunities, reach out to us: 

    Email: 
    Telegram: https://t.me/RFAIBot
   
     

Thank you for supporting RAEF.AI! 
