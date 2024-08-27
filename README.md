# AllJobs Telegram Bot
A Telegram bot built with Node.js using the [`node-telegram-bot-api`](https://github.com/yagop/node-telegram-bot-api), designed to scrape job listings from [alljobs.co.il](https://www.alljobs.co.il) using [`cheerio`](https://github.com/cheeriojs/cheerio). The bot parses HTML to extract job postings and sends only new listings directly to the user, ensuring they never miss an opportunity. A database backend tracks previously sent jobs, providing users with only the most recent updates.

## Features

- Scrapes job listings from [alljobs.co.il](https://www.alljobs.co.il) based on custom search criteria.
- Sends new job listings directly to a Telegram bot chat.
- Ensures that only new jobs are sent using a database to track previously sent jobs.

## How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/einatsof/nodejs-alljobs-telegram-bot.git
cd nodejs-alljobs-telegram-bot
```

### 2. Set Up Environment Variables
Create a .env file in the root directory and add the following variables:
```dosini
TOKEN=your-telegram-bot-token
SEARCH=freetxt=[search term]&page=1
```

- **`TOKEN`**: Your Telegram bot token. You can get this from the [BotFather](https://telegram.me/BotFather).
- **`SEARCH`**: Your custom search query for job listings. Replace [search term] with your desired job search keyword or phrase.

### 3. Install Dependencies
```bash
npm install
```

### 4. Run the Bot
```bash
npm start
```

### 5. Interact with the Bot

- Open Telegram and start a chat with your bot using the bot token you provided.
- The bot will automatically begin sending new job listings based on your search criteria.