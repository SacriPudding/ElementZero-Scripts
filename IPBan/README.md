# What is this?
This is the IP Banning script. It essentially works by creating a constant log of players IPs as well as controls
the command for banning players.

# Requirements
This script relies on another, simpler, script. `permissionHandler.js`. Its used for making sure only someone
has operator perms. It also relies on an `index.js` to actually create the listening events.
Basic list of required imports:
- `permissionHandler.js` function   
- `system` Required in every script that uses the vanilla API
- `onPlayerJoined` from ez:player
- `onChat` from ez:chat
- `sendBroadcast` from ez:chat
- `executeCommand` from ez:command
- `getPlayerByNAME` from ez:player
- `addByNAME` from ez:blacklist
- `addByXUID` from ez:player
- `open` from ez:sqlite3  
- `getOfflinePlayerByNAME` from ez:player

#### MOD REQUIREMENTS
This mod only uses the built in stuff so you don't need to worry about finding another mod to use
- `ScriptingSupport` required in every script
- `ChatAPI`
- `Blacklist` 
- `CommandSupport`

#### DATABASE REQUIREMENT
This mod requires you to use a database for storing the IPs, XUIDs, and gamertags of your players.
The database can be found here, make sure to just put it into the root directory of your server (Where the .exe is)

# Usage
In order to use this script, you must be an op and be on the server. Due to limitations, I can't read console
so you have to be in game.

For IP banning, the player you are banning DOES NOT need to be online. Banning will work whether or not said
person is online.

The default command is `.banip [gamertag]`
If you wish to change it all you have to do is adjust the `banCommand` variable inside of `IPBan.js`

# Downsides
One downside to this script is that it is not possible to ban new IPs the user joins on after they are on
the blacklist. They won't be able to get on as they are still server banned but if they make a new account
they will be able to join again.

Another downside is that the command is broadcast to chat. Meaning if you are banning someone while people are online those people will know.

# Known bugs
None! Go ahead and send me a message if you find one!
#### Social medias:
- Twitter: https://twitter.com/SacriPudding
- Discord: @SacriPudding#1281
- Telegram: @SacriPudding
- Reddit: https://reddit.com/u/evan13lee
- GitHub: https://github.com/SacriPudding (Crazy I know)

# Plans
- VPN detection VIA GeoIP
- Console based command. (Need to find some way to talk to console. Currently in development.) 
- Losing the need for `index.js` opting for a drag-and-drop system.

# Credits
A lot of this came from my friend Luke. This was my first "real" plugin and also one of my first JS scripts
in general. Follow him over at https://twitter.com/ConsoleLogLuke. He is into mostly iPhone jailbreaking.
