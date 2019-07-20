<img width="230" height="150" align="left" style="float: left; margin: 0 10px 0 0;" alt="Atlanta" src="https://www.stop-cybersexisme.com/sites/default/files/youtube-1837872_640.png">

# Discord Youtube Notifier

[![CodeFactor](https://www.codefactor.io/repository/github/androz2091/discordyoutubenotifier/badge)](https://www.codefactor.io/repository/github/androz2091/discordyoutubenotifier)
[![](https://img.shields.io/discord/565048515357835264.svg?logo=discord&colorB=7289DA)](https://discord.atlanta-bot.fr)
[![](https://img.shields.io/badge/patreon-donate-orange.svg)](https://www.patreon.com/androz2091)

> This bot is not available for invite.

**Discord Youtube Notifier** bot allows you to receive your Youtube notifications directly on Discord!

## Features

🚩 Use of the simple RSS technology  
▶️ Unlimited YouTubers support (you can add as many as you want)  
🌐 Automatic resolving Youtube channels URLs  
📝 Custom messages for announcements messages  

## How it works?

Here is a simplified explanation of how the bot works:

*   Every 20 seconds, a function queries Youtube (using RSS) to get the latest video from the Youtuber.

*   If a video is found, it is checked twice:
    -   Was the video published after the bot started?  
    -   Hasn't the video already been posted on Discord?  

*   Then, the video is sent on discord

## Edit config

You must edit the configuration file for the bot to work correctly:

```Json
{
    "token": "your-discord-bot-token-here",
    "message": "New video **{videoTitle}** by **{videoAuthorName}** uploaded at **{videoPubDate}**! Link: {videoURL}",
    "channel": "your-channel-id-for-announcements-here",
    "youtubers": [
        "Pewdiepie",
        "Squeezie",
        "https://www.youtube.com/channel/UCNuYih-JMtLxOlsjeIos4ZA"
    ],
    "youtubeKey": "your http://console.developer.google.com youtube v3 api key"
}
```

**token**: your discord bot token  
**message**: the message that will be sent in the announcement channel when a new video is uploaded  
**channel**: the id of the announcement channel  
**youtubers**: an array of your subscriptions, this can be a youtuber name or a youtuber channel url  
**youtubeKey**: your youtube api v3 api key. It can be found [here](https://developers.google.com/youtube/v3/getting-started)  