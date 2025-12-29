# SpareRoom Parser
**Python 3.10+**


A concise one-sentence description of what your bot actually does (e.g., "An automated bot for tracking GitHub repository releases and notifying users in real-time").

## 🚀 Features

* **Automated Scraping:** Periodically parses SpareRoom listings based on your custom parameters (location, price, etc.).
* **Telegram Integration:** Receive instant alerts and manage your search directly through the Telegram interface.
* **Docker Ready:** Fully containerized, allowing it to run seamlessly on any machine, server, or VPS.
* **Persistent Tracking:** Uses SQLite to keep track of viewed listings, so you never receive the same notification twice.

## 🛠 Tech Stack

* **Language:** Python
* **Scraping:** Selenium & BeautifulSoup4 (BS4)
* **Bot Framework:** Aiogram
* **Database:** SQLite

## 📋 Prerequisites

Before you begin, ensure you have:
1.  A **Telegram Bot Token** (obtain from [@BotFather](https://t.me/botfather)).
2.  **Python 3.10+** or **Docker** installed on your system.
   

## ⚙️ Installation & Setup

1. **Clone the repository:**
```bash
git clone https://github.com/maksymrusanov/telegram-bot.git
cd telegram-bot
```
  2. **Configure Environment Variables**
Create a .env file in the root directory and add your bot credentials:
```bash
BOT_TOKEN=your_telegram_bot_token_here
ADMIN_ID=your_telegram_user_id
```
3. **Create Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # Linux / macOS
venv\Scripts\activate     # Windows
```
4. **Choose Your Run Method**

**Option A: Running with Docker (Recommended)**
This method is the most reliable as it handles all browser drivers and dependencies automatically.
```bash
# Build the image
docker build -t spare-room-bot .

# Run the container
docker run -d --name spare-room-bot --env-file .env spare-room-bot
```
Option B: Running Locally

a) **Create and activate a virtual environment:**
```bash
python -m venv venv
source venv/bin/activate  # Linux / macOS
venv\Scripts\activate     # Windows
```
b) **Install dependencies:**
```bash
pip install -r requirements.txt
```
c) **Launch the bot:**
```bash
python bot-main.py
```
