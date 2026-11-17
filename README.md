# CoinTraVert

**A desktop currency converter with live exchange rates, user accounts and conversion history.**

CoinTraVert converts between world currencies using real-time rates from the ExchangeRate API. Each user has their own account, and every conversion is saved to a personal history so it can be reviewed later.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![CustomTkinter](https://img.shields.io/badge/CustomTkinter-1F6FEB)
![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite&logoColor=white)
![ExchangeRate API](https://img.shields.io/badge/ExchangeRate--API-2EA44F)

---

## Features

- **User accounts:** sign up and log in, with duplicate-email and input validation
- **Live currency conversion:** converts any supported currency pair using real-time rates
- **One-click swap:** switch the "from" and "to" currencies instantly
- **Peso rate board:** shows what 1 Philippine peso is worth in other currencies
- **Conversion history:** every conversion is saved per user with its date and time
- **Account settings:** update display name, email and password, and log out

## Security

- Passwords are hashed with **PBKDF2-HMAC-SHA256** and a unique random salt per user. Plain-text passwords are never stored.
- Password checks use a constant-time comparison.
- The API key is loaded from a local `.env` file and is never committed to the repository.
- All database queries use parameterized statements.

## Tech Stack

| Area | Technology |
|---|---|
| Language | Python 3 |
| User interface | CustomTkinter, Tkinter, Pillow |
| Database | SQLite |
| Exchange rates | [ExchangeRate API](https://www.exchangerate-api.com) via `requests` |

## Project Structure

```
CoinTraVert/
├── main.py               # Application: sign up, login, converter, history, settings
├── currency_spec.json    # Currency names and display colors
├── requirements.txt      # Python dependencies
├── .env.example          # Template for the API key
└── *.png / *.jpg         # Logos, icons and backgrounds
```

## Getting Started

### Prerequisites

- Python 3
- A free API key from [exchangerate-api.com](https://www.exchangerate-api.com)

### Installation

```bash
git clone https://github.com/yeldsg/cointravert.git
cd cointravert
pip install -r requirements.txt
```

### Configuration

Copy `.env.example` to `.env` and add your API key:

```
EXCHANGE_RATE_API_KEY=your_api_key_here
```

### Run

```bash
python main.py
```

The SQLite database (`cointravert.db`) is created automatically on first launch.

## About This Project

CoinTraVert was built as a team project for a programming course (October – December 2025).

## Author

**Kathrina Marhiel Zamora** · BS Information Technology, Pampanga State University
GitHub: [@yeldsg](https://github.com/yeldsg)
