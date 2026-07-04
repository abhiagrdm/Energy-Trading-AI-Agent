# ⚡ Autonomous Energy Trading Desk

An AI-powered market surveillance system for Indian energy stocks, built with a multi-agent architecture. It fetches live market data, gathers news intelligence via Perplexity AI, and generates a trading decision (CHARGE / DISCHARGE / HOLD) for grid-connected battery storage systems.

---

## Demo

> Built with Streamlit — runs entirely in your browser.

---

## How It Works

The app uses a **3-agent pipeline** orchestrated by LangGraph:

1. **Market Data Agent** — Fetches live stock price and 5-day performance using `yfinance`
2. **Research Agent** — Queries Perplexity AI (`sonar-pro`) for the latest news on coal supply, government energy policy, and renewable projects
3. **Trader Agent** — Combines market data + news context and outputs a final **CHARGE / DISCHARGE / HOLD** signal

---

## Tech Stack

| Layer | Tool |
|---|---|
| Frontend | [Streamlit](https://streamlit.io/) |
| Agent Orchestration | [LangGraph](https://www.langchain.com/langgraph) |
| Market Data | [yfinance](https://pypi.org/project/yfinance/) |
| AI / LLM | [Perplexity AI](https://www.perplexity.ai/) (`sonar-pro`) |

---

## Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/abhiagrdm/Energy-Trading-AI-Agent.git 
cd YOUR_REPO_NAME
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Get a Perplexity API Key

Sign up at [perplexity.ai](https://www.perplexity.ai/settings/api) and generate an API key.

### 4. Run the app

```bash
streamlit run PowerTrading_AgAI.py
```

---

## Usage

1. Enter your **Perplexity API Key** in the sidebar
2. Type the **Company Name** (e.g., `Tata Power`) and its **NSE ticker** (e.g., `TATAPOWER.NS`)
3. Click **Initialize Trading Agent**
4. View the live signal: **CHARGE**, **DISCHARGE**, or **HOLD**

---

## Project Structure

```
├── PowerTrading_AgAI.py   # Main application
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

*Author: Abhishek Agrawal · MBA Finance · 2026*
*Connect: https://www.linkedin.com/in/abhisheka24 · abhishek.iitk.mba@gmail.com*
