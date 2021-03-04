# JokeBot
A joke bot that can be added as an overlay to a stream

## Installation
### Download
You can either clone the entire repo or download the only file in it.

To download the repo:
```
# with ssh
git clone git@github.com:fendull-streamer/JokeBot.git

# with https
git clone https://github.com/fendull-streamer/JokeBot.git
```


To download `joke.html` directly, right click [THIS LINK](https://raw.githubusercontent.com/fendull-streamer/JokeBot/master/joke.html) and click "Save link as..." 

### File modifications
Open `joke.html` with a text editor. On lines 9-13, you should see the following:

```
const CHANNEL = "fendull"; //The channel you want the joke bot to speak to
const BOT_USERNAME = "fendull"; //The name of the account the bot assumes
const OAUTH_TOKEN = "oauth:xxxxxxxxxxxxxxx"; //the oauth token retrieved from https://twitchapps.com/tmi/ while logged in as the above account
//Make sure no one can copy your oauth token, otherwise they may be able to chat from your account
const TIME_UNTIL_PUNCHLINE = 20; //Time in seconds between the initial line of the joke and the punchline
```

1. On the line with CHANNEL, replace `fendull` with your channel name
2. On the line with BOT_USERNAME, replace `fendull` with your channel name or name of the account you want to speak the joke
3. On the line with OAUTH_TOKEN, replace `oauth:xxxxxxxxxxxxxxx` with the value obtained from [https://twitchapps.com/tmi/](https://twitchapps.com/tmi/). Make sure you are currently logged into Twitch with the account you listed on the line above
4. On the line with TIME_UNTIL_PUNCHLINE, replace 20 with however many seconds you want the bot to wait until speaking the punchline

## OBS set up
1. Create a new browser source and select the option for "Local file" if present.
2. Set joke.html as the local file used for the browser source
3. Select "Shutdown source when not visible" and "Refresh browser source when scene becomes active"

## Usage
- Simply activate the browser source to begin telling a joke!
- To tell another joke, deactivate the source and reactivate it.
