# CoinTraVert

A desktop currency converter built with Python and CustomTkinter. It uses live exchange rates from the ExchangeRate API and keeps each user's conversion history in SQLite.

## Features

- Sign up and log in (passwords are stored as salted PBKDF2 hashes)
- Convert between currencies using live rates
- Swap the "from" and "to" currencies in one click
- See how much 1 Philippine peso is worth in other currencies
- View your conversion history (audit trail)
- Settings: change display name, email and password, and log out

## Tech stack

Python, CustomTkinter, Pillow, SQLite, ExchangeRate API

## Run it locally

1. Install the packages:
   ```
   pip install -r requirements.txt
   ```
2. Get a free API key at https://www.exchangerate-api.com
3. Copy `.env.example` to `.env` and paste your key:
   ```
   EXCHANGE_RATE_API_KEY=your_api_key_here
   ```
4. Start the app:
   ```
   python main.py
   ```

The database file `cointravert.db` is created automatically the first time you run the app.
