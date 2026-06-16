# Live Trading Bot

A production-ready trading bot with live price streaming, 
state machine architecture and persistent trade logging.

## What This Project Does
- Simulated broker with buy/sell/cash tracking
- Live price streaming fetching real market data every 5 seconds
- State machine managing bot behavior (IDLE → SCANNING → IN_POSITION → EXITING)
- Retry logic and error handling for reliability
- Heartbeat monitor to detect if bot goes silent
- SQLite database storing every trade permanently
- Daily P&L report generated automatically

## Results
- Bot ran 203 heartbeats on QQQ 2024 data without crashing
- All trades saved to database and survived restarts
- Telegram alerts firing on every trade and error

## Tech Stack
- Python 3.12
- yfinance
- SQLite3
- logging
- requests (Telegram API)

## How to Run
```bash
pip install pandas yfinance requests
python bot.py
```

## Key Files
- `bot.py` — Main trading bot
- `state_machine.py` — State manager
- `broker.py` — Simulated broker
- `database.py` — SQLite trade logging
- `alerts.py` — Telegram notifications

## Architecture
