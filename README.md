# CVE-Bot-Notif

```
_____________   _______________            _______   ___________________.______________
\_   ___ \   \ /   /\_   _____/            \      \  \_____  \__    ___/|   \_   _____/
/    \  \/\   Y   /  |    __)_    ______   /   |   \  /   |   \|    |   |   ||    __) 
\     \____\     /   |        \  /_____/  /    |    \/    |    \    |   |   ||     \ 
 \______  / \___/   /_______  /           \____|__  /\_______  /____|   |___|\___  /
        \/                  \/                    \/         \/                  \/1.0
```

> Fork of [BotPEASS](https://github.com/carlospolop/BotPEASS/)

Use this bot to monitor new CVEs containing defined keywords and send alerts to Slack, Telegram, Discord, Pushover and/or MS Teams. 

## Configure one for yourself

**Configuring your own BotPEASS** that notifies you about the new CVEs containing specific keywords is very easy!

- Fork this repo
- Modify the file `config/bopteas.yaml` and set your own keywords
- In the **github secrets** of your forked repo enter the following API keys:
    - **VULNERS_API_KEY**: (Optional) This is used to find publicly available exploits. You can ue a Free API Key.
    - **SLACK_WEBHOOK**: (Optional) Set the slack webhook to send messages to your slack group
    - **DISCORD_WEBHOOK_URL**: (Optional) Set the discord webhook to send messages to your discord channel
    - **TELEGRAM_BOT_TOKEN** and **TELEGRAM_CHAT_ID**: (Optional) Your Telegram bot token and the chat_id to send the messages to
    - **PUSHOVER_DEVICE_NAME**, **PUSHOVER_USER_KEY** and **PUSHOVER_TOKEN**: (optional) Set the pushover information to send the message
    - **MSTEAMS_WEBHOOK** (Optional) Set the Microsoft Teams webhook to send messages to your Microsoft Teams channel 
- Check `.github/wordflows/bopteas.yaml` and configure the cron (*once every 8 hours by default*)

*Note that the slack, telegram, pushover and discord configurations are optional, but if you don't set any of them you won't receive any notifications anywhere*
