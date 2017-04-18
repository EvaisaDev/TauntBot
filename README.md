 # TauntBot
TauntBot is based on Airhorn Bot and requires Go 1.4 or higher.

## Usage
TauntBot has two components, a bot client that handles the playing of loyal airhorns, and a web server that implements OAuth2 and stats.


### Running the Bot

**First install the bot:**
```
go get https://github.com/EvaisaGiac/TauntBot/cmd/bot
go install https://github.com/EvaisaGiac/TauntBot/cmd/bot
```
 **Then run the following command:**

```
bot -r "localhost:6379" -t "MY_BOT_ACCOUNT_TOKEN" -o OWNER_ID
```

### Running the Web Server
First install the webserver: `go install https://github.com/EvaisaGiac/TauntBot`, then run `make static`, finally run:

```
./tauntweb -r "localhost:6379" -i MY_APPLICATION_ID -s 'MY_APPLICATION_SECRET"
```

Note, the webserver requires a redis instance to track statistics
