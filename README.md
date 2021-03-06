# AragonDAO Bot
Telegram and Discord bots to integrate groups with Aragon.
## Project Description
Our project is aimed to bring the communites and social groups closer to Aragon DAO. Our project has two bots, discord bot and telegram bot, running on same modular codebase. Users can get links to allocate funds, that is to create proposal and withdrawls, see all the proposals etc.
Some of the features are:- 
1. Listing proposals.
2. Listing transactions.
4. Getting link to create proposals.
3. Getting link to create withdrawl requests.
3. Bot sends a text to group when a new transaction is made to or from the bot.
4. Bot sends a text to group when a new proposal is created in the DAO.
5. Above two features makes our bot work as a notification service as well.
6. Showing balance of DAO.
7. Sending necessary links to the group related to DAO whenever required.
8. Project is on simple docker container so it can run on any system.

## Instructions to run the project
* Run with docker
  - Add a firebase config file in `bot-app/src` with name `firebase-config.json` and make sure you have firestore enabled.
  - Add your telegram access token in `bot-app/src/TelegramBot/config.json` and discord access token in `bot-app/src/DiscordBot`.
  - For first run build the project with `docker-compose up --build`
  - For consequent runs you can simply run it with `docker-compose up`
* Run with yarn, follow the given commands
  - Add your telegram access token in `bot-app/src/TelegramBot/config.json` and discord access token in `bot-app/src/DiscordBot`.
  - Add a firebase config file in `bot-app/src` with name `firebase-config.json` and make sure you have firestore enabled.
  - `cd bot-app`
  - `npm install`
  - `npm install yarn -g`
  - `npm run dev`
## Adding bot to your group
* Below given bot are already hosted on our server.
* Telegram 
  - Add this bot to your group http://t.me/aragondao69_bot
  - Run `/register DAOName 0xDaoAddress`
* Discord 
  - Add this bot to your server https://discord.com/api/oauth2/authorize?client_id=737272433802870875&permissions=8&scope=bot
  -  Run `!register DAOName 0xDAOAddress`
## List of Commands
* Telegram
  - `/start` This can be used to get some initial instructions.
  - `/register` This can be used to register your DAO to bot in a group.
    - Example - `/register superDAO 0x2Ee331840018465bD7Fe74aA4E442b9EA407fBBE`
  - `/proposals` List all the proposals of the DAO.
  - `/transactions` List all the transactions.
  - `/token` Gives information about DAO member token.
  - `/balance` Gives ETH present in DAO.
  - `/dao` Gives link to the DAO.
  - `/newpoposal` Gives a link to create new proposal.
  - `/newtransaction` Gives a link to create deposit or withdraw from DAO.
* Discord
  - `!help` This can be used to get help with some command and get list of commands.
  - `!register` this can be used to register your DAO to bot in a group.
    - Example - `!register superDAO 0x2Ee331840018465bD7Fe74aA4E442b9EA407fBBE`
  - `!proposals` List all the proposals of the DAO.
  - `!transactions` List all the transactions.
  - `!token` Gives information about DAO member token.
  - `!balance` Gives ETH present in DAO.
  - `!dao` Gives link to the DAO.
  - `!newpoposal` Gives a link to create new proposal.
  - `!newtransaction` Gives a link to create deposit or withdraw from DAO.
## Project Team
1. Mitrasish Mukherjee
    * Github - https://github.com/rekpero
    * Role - 
        * Developed the bots.
        * Made whole code modular.
        * Improved the UX a lot.
        * Made code of telegram bot and Discord bot consistent and similar.
        * Designed the architecture for the code base for bots to have as much common code as possible.
2. Abhimanyu Shekhawat 
    * Github - https://github.com/Abhimanyu121
    * Role - 
        * Handeled interaction with Aragon DAO.
        * Communicated with Aragon Team for resolving road blockers.
        * Made interaction with database to keep track of all the groups.
        * Worked on workflow.
<br>

## A prototype
1. Github link - 
    * https://github.com/rekpero/DaoFatherBot
2. Link to demo video - 
    * https://drive.google.com/file/d/10QZL2l_UVnOcM4Dh24vvdfhq_OixkGYp/view?usp=sharing


### Notes
1. Product is still in beta stage so it might have some bugs.
2. Due to late response from Aragon subgraph some commands may take a few second to respond.
3. Whenever a new transaction is recieved bot sends a text on group but it might take from a few seconds to a few minutes.
4. Make sure you enter correct information while registering your DAO.

## Future Scopes
1. If aragon team likes it, taking it further with Aragon's support.
2. Showing more information in the group itself.
3. Requesting more features from Aragon in their Aragon Connect to make this bot even better.
4. Making the bot more responsive.

