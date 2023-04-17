## Installation | How to use the Bot

**1.** Install [node.js v12](https://nodejs.org/api/cli.html#cli_unhandled_rejections_mode) or higher

**2.** Download this repo and unzip it | or git clone it

**3.** Install all of the packages with **`npm install`** | the packages are **`npm install `**

**3.1** Fill in everything in config.json

**4.** start the bot with **`node index.js`**

### Usage - index.js

```javascript
const Discord = require("discord.js"); //load the Discord.js Library
const client = new Discord.Client(); //make a new Client
const config = require("./config.json"); //load in all of the config files
client.on("ready", () => console.log("READY")); //log when the bot gets ready
const welcome = require("./welcome"); //load the transcript.js file
welcome(client); //call the transcript file with the client, the COMMAND, and the maximum of messages to fetch
client.login(config.TOKEN); //start the bot with the bot token
```

### Usage - config.json

- "TOKEN" ... is your Bot token
- "CHANNEL_WELCOME" ... is the Channel ID of your welcome channel
- "ROLES_WELCOME" ... are all of the Role IDs you wanna add to the user when he joins the server, it must be an array and can be unlimited!

```json
{
  "TOKEN": "",
  "CHANNEL_WELCOME": "",
  "ROLES_WELCOME": ["", ""]
}
```
