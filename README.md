# AI Image Generator Telegram Bot

A powerful Telegram bot that transforms text descriptions into stunning AI-generated images. Simply send a text prompt, and the bot will create a unique image based on your description. The bot leverages advanced AI image generation technology to turn your imagination into visual art.

This bot is designed to be user-friendly and accessible to everyone, supporting both English and Arabic inputs. It automatically translates non-English text, ensuring a seamless experience for users worldwide. With features like loading animations, error handling, and admin controls, it provides a robust platform for creative expression through AI.

Perfect for creative projects, content creation, brainstorming visual ideas, or just having fun with AI art generation - all within the familiar Telegram interface.

## Features

- **AI Image Generation**: Convert text descriptions into images using AI
- **Multilingual Support**: Automatically translates Arabic text to English for processing
- **User Management**: Tracks users in a SQLite database
- **Admin Controls**: Special commands for administrators
- **Broadcast Functionality**: Send messages to all registered users
- **Mandatory Subscription**: Option to require users to subscribe to specific channels/groups
- **Error Reporting**: Automatic error notifications to administrators
- **Loading Animations**: Visual feedback during image generation
- **Configurable Settings**: All bot settings stored in a JSON configuration file

## Setup

### Prerequisites

- Python 3.6+
- Telegram Bot Token (from [@BotFather](https://t.me/BotFather))
- API access for the AI image generation service

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/jj611a/telegram-AI-pic-generator.git
   cd telegram-AI-pic-generator
   ```

2. Set up a virtual environment (recommended):
   
   **On Windows:**
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
   
   **On macOS/Linux:**
   ```
   python3 -m venv venv
   source venv/bin/activate
   ```
   
   *Note: After activation, your command prompt should show `(venv)` at the beginning, indicating the virtual environment is active.*

3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Configure the bot by editing `config.json`:
   ```json
   {
       "bot_token": "YOUR_BOT_TOKEN",
       "botuser": "YOUR_BOT_USERNAME",
       "admins": [YOUR_TELEGRAM_ID],
       "subscription_channels_groups": [],
       "new_user_notification": true
   }
   ```

5. Run the bot:
   ```
   python bot_pic.py
   ```

## Usage

### User Commands

- `/start` - Start the bot and register as a user
- Send any text message to generate an image based on the description

### Admin Commands

- `/بث` (Broadcast) - Reply to a message to broadcast it to all users
- `/s` (Stats) - Get statistics about the bot usage

## Configuration

The `config.json` file contains all the bot settings:

- `bot_token`: Your Telegram bot token
- `botuser`: Your bot's username (without @)
- `admins`: List of Telegram user IDs who have admin privileges
- `subscription_channels_groups`: List of channels/groups users must subscribe to
- `new_user_notification`: Whether to notify admins when a new user starts the bot

## Error Handling

The bot includes robust error handling with automatic reporting to administrators and self-recovery mechanisms to ensure continuous operation.

## License

[MIT License](LICENSE)

## Acknowledgements

- [pyTelegramBotAPI](https://github.com/eternnoir/pyTelegramBotAPI) for the Telegram bot framework
- [deep-translator](https://github.com/nidhaloff/deep-translator) for translation capabilities
- [Pillow](https://python-pillow.org/) for image processing

---

Created with ❤️ by [Your Name] 
