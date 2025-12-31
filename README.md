# Telegram Summarizer Bot 🤖📚

## About the Bot
This Telegram bot summarizes messages from a group chat based on a selected time range (e.g., last 12 hours, 1 day, 1 week) or message count. It uses Google Gemini API to generate concise summaries, making it easier for users to catch up on important discussions.

## Why I Built This Bot
I often miss out on reading all the messages in my group chats due to a busy schedule. This bot helps me stay informed by providing a summarized overview of key discussions over a selected period.

## Features
✅ Log messages from a Telegram group chat  
✅ Summarize messages based on:
   - **Time ranges**: `12 hours`, `1 day`, `1 week`, etc.
   - **Message count**: Last N messages (e.g., last 50, last 100 messages)
✅ Uses **Google Gemini API** for high-quality AI-powered summaries
✅ API keys stored securely as environment variables  
✅ Lightweight and fast - no local AI models to download  

## How to Use
1. **Start the bot** by adding it to your group chat.
2. Use `/start` to see all available options.
3. Use `/summarize <option>` to get a summary:
   - **Time-based**: `/summarize 1day`, `/summarize 12hr`, `/summarize 1week`
   - **Count-based**: `/summarize last 50`, `/summarize last 100` (summarizes last N messages)

## Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/SamNm89/Telegram_Summarizer_Bot.git
   cd Telegram_Summarizer_Bot
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables:**
   - Copy `.env.example` to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Edit `.env` and add your secrets:
     - `TELEGRAM_BOT_TOKEN`: Your Telegram Bot Token (get it from [@BotFather](https://t.me/BotFather))
     - `GOOGLE_API_KEY`: Your Google API key (required)
       - Get your API key from [Google AI Studio](https://makersuite.google.com/app/apikey)

4. **Run the bot:**
   ```bash
   python telegram_bot.py
   ```

## Requirements
- Python 3.7+
- `pyTelegramBotAPI` - Telegram bot API wrapper
- `pandas` - Data manipulation
- `python-dotenv` - Environment variable management
- `google-generativeai` - Google Gemini API

**Note:** This bot uses Google Gemini API exclusively. No local AI models are required, making it lightweight and fast to install (~50-70 MB total).

## Deployment
To keep the bot running continuously on a server, use:
```sh
nohup python telegram_bot.py &
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



**Forked & Enhanced by:** SamNm89  


