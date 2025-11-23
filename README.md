# Discord Music Bot

A feature-rich Discord music bot written in Python using [discord.py](https://github.com/Rapptz/discord.py) and [yt-dlp](https://github.com/yt-dlp/yt-dlp). This bot can play music from YouTube, manage queues, control volume, and supports both prefix and slash commands.

# Before you clone this repo yoy need to set up bot on Discord Aplication:
Goal: Create the bot identity, get the password (Token), and give it permission to hear.

Create the Application:
- Go to the Discord Developer Portal.
- Click "New Application" (top right).
- Name it (e.g., MusicBot) and click Create.

Create the Bot User:
- On the left menu, click Bot.
(Optional) Upload an icon for your bot.
- Copy the Token: Click "Reset Token" -> "Yes, do it!".
IMPORTANT: Copy this long string immediately. This is your bot's password. Do not share it.

Enable Privileged Intents (Crucial):
- Still on the Bot page, scroll down to the "Privileged Gateway Intents" section.
- Enable (Turn ON) all three switches:
-Presence Intent
- Server Members Intent
- Message Content Intent (If this is off, your commands will fail).
- Click "Save Changes" at the bottom.

Invite the Bot to your Server:
- On the left menu, click OAuth2 -> URL Generator.
- Under Scopes, check: bot and applications.commands.
Under Bot Permissions, check: Administrator (easiest for testing) or specifically Connect, Speak, Send Messages.

Copy the Generated URL at the bottom, paste it into your browser, and invite the bot to your server.
## Features

- Play music from YouTube links or search queries
- Playlist support (up to 5 songs per playlist)
- Queue management (view, add, clear)
- Volume control (0-200%)
- Pause, resume, and stop playback
- Join and leave voice channels
- Supports both prefix (`$`) and slash (`/`) commands
- Logging for easier debugging

## Requirements
- Python 3.8+
- [discord.py](https://pypi.org/project/discord.py/) (`pip install -U discord.py`)
- [yt-dlp](https://pypi.org/project/yt-dlp/) (`pip install -U yt-dlp`)
- [python-dotenv](https://pypi.org/project/python-dotenv/) (`pip install -U python-dotenv`)
- FFmpeg (must be installed and in your system PATH) https://www.gyan.dev/ffmpeg/builds/

## Setup

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/discord-music-bot.git
    cd discord-music-bot
    ```

2. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3. **Create a `.env` file:**
    ```
    DISCORD_TOKEN=your_discord_bot_token_here
    ```

4. **Run the bot:**
    ```bash
    python bot.py
    ```

## Usage

### Prefix Commands (`$`)

- `$join` — Bot joins your voice channel
- `$play <url or search>` — Play a song or add to queue
- `$queue` — Show current queue
- `$volume <0-200>` — Set playback volume
- `$pause` — Pause playback
- `$resume` — Resume playback
- `$stop` — Stop and clear queue
- `$leave` — Bot leaves the voice channel

### Slash Commands

Type `/` in Discord and select the bot's commands:
- `/join`
- `/play`
- `/queue`
- `/volume`
- `/pause`
- `/resume`
- `/stop`
- `/leave`

## Notes

- The bot will only play audio in voice channels.
- Make sure the bot has permission to join and speak in your voice channel.
- For best results, use the latest version of FFmpeg.

## License

MIT License

---

**Enjoy your music!**
