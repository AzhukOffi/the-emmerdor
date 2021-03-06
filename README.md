# theemmerdor

With this module, you have the possibility to configure the sounds played when a given user enters a discord channel.

It quickly becomes annoying for him

## Install

``` bash
npm i
```

## Get a discord token

Go [here](https://discord.com/developers/applications).

Click on ``` New application ```

Go to ```bot``` and ```add bot```

You can get your token when you click on ```Click to Reveal Token```


## Usage

``` bash
DISCORD_TOKEN=<your bot token\> CHANNEL_ID=<channel to send msg> PASSWORD=<a password to secure frontend\> nodemon --ext js src/index
```

Available command in discord: 

| Command  | Description  | 
|---|---|
| /isAlive  | Check if service is online or not  |
| /list  | Display all trigger configured for each users  |
| /help  | Display all command available  |

## Deploy
This bot is automatically deploy to production when a tag is created.

A docker version is upload [here](https://github.com/clabroche/docker-registry/packages/466346
)

An exemple of [docker-compose.yml](https://github.com/clabroche/the-emmerdor/blob/master/docker-compose.yml) is present on this repository 

## Architecture
- configs // Where config are stored for persistence
- sounds // Where sound are stored for persistence
- src  // All source code 
  - front // admin front end 
  - index.js // bot entrypoint
  -  server.js // server launched on bot startup

## Contribute

Your commit should be in [this format](https://github.com/commitizen/cz-cli)

Make me some PR. I will merge and make a tag to deploy automatically the bot to prod