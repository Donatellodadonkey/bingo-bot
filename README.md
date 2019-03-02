# Bingo Bot

LittleBigPlanet speedrunning race bot for Discord.

# Setup

Install nodejs (version 6.x or higher).

Get build tools.
* Windows: Install "VC++ 2015.3 v14.00 (v140) toolset for desktop" through VS Installer
* Linux: `sudo apt-get install build-essential`

Get dependencies.

* `npm init -y`
* `npm i discord.js node-gyp better-sqlite3`

Create config.json in same directory as bob.js with your auth token.

```
{
    "token": "discord auth token goes here"
}
```

Run bot

```
node bob.js
```

# Features

**Pre-race commands**

* `!race` - Starts a new full-game race, or joins the current open race if someone already started one.
* `!game <game name>` - Sets the game (e.g. `!game LBP2`)..
* `!category <category name>` - Sets the category (e.g. `!category styrofoam%`).
* `!exit` - Leave the race.
* `!ready` - Indicate that you're ready to start.
* `!unready` - Indicate that you're not actually ready.

**Mid-race commands**
* `!d` / `!done` - Indicate that you finished.
* `!ud` / `!undone` - Get back in the race if you finished by accident.
* `!f` / `!forfeit` - Drop out of the race.
* `!uf` / `!unforfeit` - Rejoin the race if you forfeited by accident.

**Stat commands**
* `!status` - Shows current race status/entrants.
* `!me <game name>` - Shows your race statistics for the specified game (e.g. \`!me LBP\` shows your LBP1 stats).
* `!results <race num>` - Shows results of the specified race number (e.g. \`!results 2\`).
* `!help` - Shows the bot commands.

**Admin/moderator only**
* `!kick @user` - Kicks someone from the race (in case they're afk or something).
* `!endrace` - Forces ending the race without recording any results.

# Upcoming Features?

## Stuff I definitely want to do:
* `!ilrace` - Start a series of individual level races.

## Stuff I kinda want to do but might be too lazy:
* `!coop` - Start a co-op race.
* `!elo <game name>` - Shows an ELO leaderboard for each category in the given game.