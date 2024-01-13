![Screenshot (230)](https://github.com/someoneskilled/MoodAnalyzerBot/assets/134536864/0e77627b-2836-4d4a-a672-1feed7be1384)

# Mood Analyzer Bot

This is a simple Telegram bot that analyzes the mood of user messages in a chat, based on both text sentiment analysis and emoji sentiment. The bot uses the Natural Language Toolkit (nltk) library for text sentiment analysis and a pre-defined dictionary for emoji sentiment. The sentiment analysis is used to classify messages into positive, negative, or neutral categories.

## Features
- **Text Sentiment Analysis:** The bot utilizes the VADER sentiment analysis tool from nltk to determine the sentiment (positive, negative, neutral) of the user's text messages.
- **Emoji Sentiment Analysis:** The bot extracts emojis from the messages and assigns sentiments based on a pre-defined dictionary (`emoji_sentiments.json`).
- **Bot Response:** The bot responds to user messages with an appropriate sentiment label (e.g., Positive, Negative, Neutral) or a sentiment derived from the most common sentiment associated with the emojis used in the message.
- **Telegram Commands:**
  - `/start`: Initiates a conversation with the bot.
  - `/help`: Provides help information.

## How it Works
1. The bot processes incoming messages, extracting text and emojis.
2. The VADER sentiment analysis tool analyzes the text to determine its sentiment.
3. Emojis are matched with pre-defined sentiments in the `emoji_sentiments.json` file.
4. The bot combines text and emoji sentiments to generate a final mood classification.
5. The bot responds to the user or group based on the calculated mood.

## Requirements
- Python 3.x
- nltk library
- emoji library
- regex library
- python-telegram-bot library

## Setup
1. Install the required libraries using:
   ```
   pip install nltk emoji regex python-telegram-bot
   ```
2. Download NLTK data:
   ```python
   import nltk
   nltk.download('vader_lexicon')
   ```
3. Replace the `token` variable in the code with your own Telegram bot token.
4. Run the script.

## Notes
- The bot currently supports English text sentiment analysis.
- Adjustments to the sentiment analysis thresholds can be made based on your preferences.

Feel free to customize and enhance the bot according to your needs. Happy coding!
