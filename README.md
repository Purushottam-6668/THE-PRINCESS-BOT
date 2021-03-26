<h1 align="center">Hi 👋 HEY THIS IS PRINCESS😊💫</h1>
<p align="center">
<br>
<p align="center">
<a href="https://github.com/PURHSHOTTAM/PRINCESS"><img src="https://telegra.ph/file/79b6e92a2bc2e845cc611.jpg" alt="https://github.com/PURHSHOTTAM/PRINCESS" height=300px, width=720px></a>
<br>
   
<br>
<p align="left"> <img src="https://komarev.com/ghpvc/?username=PURUSHOTTAM&label=Profile%20views&color=0e75b6&style=plastic" alt="PURUSHOTTAM" /> </p>

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/PURHSHOTTAM/PRINCESS)

# CREDITS 
- 🔭 CODE OWNER (DEVLOPER)[`𓊈𒆜𝙼𝚛_𝙿𝚞𝚛𝚞𝚜𝚑𝚘𝚝𝚝𝚊𝚖𒆜𓊉`](http://t.me/Mr_Purushottam_M)
- 💠 CURRENTLY OWNER AT [`LIBRARIAN_INSTITUTE`](https://t.me/Channel_Librarian)
- 💠 CO OWNER OF LIBRARIAN [`ANIMESH VERMA`](https://t.me/AniMesH941)
 - 💠 MY FRIEND `[SANGRAAM`](https://t.me/sangramghangale)
- 💠 SUPPORT GROUP FOR [`𓊈𒆜Princess Support𒆜𓊉`](https://t.me/PRINCESS_SUPPORT)
- 📫 SUCCESSED VERSION OF PRINCESS **Telegram -[`𓊈𒆜𝙿𝚁𝙸𝙽𝙲𝙴𝚂𝚂𒆜𓊉`](https://t.me/The_Princess2_Bot)**



[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)](https://github.com/ellerbrock/open-source-badges/)  
[![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html)

Modular Telegram bot for managing your groups with a extras features with HunterxHunter theme.

<p align="center">
  <a href="https://github.com/PURUSHOTTAM/PRINCESS/fork">
    <img src="https://img.shields.io/github/forks/PURUSHOTTAM/PRINCESS?label=Fork&style=social">
    
  </a>
  <a href="https://github.com/PURUSHOTTAM/PRINCESS">
    <img src="https://img.shields.io/github/stars/PURUSHOTTAM/PRINCESS?style=social">
  </a>
</p>
```
There are two possible ways of configuring your bot: a config.py file, or ENV variables.

The prefered version is to use a `config.py` file, as it makes it easier to see all your settings grouped together.
This file should be placed in your `cinderella` folder, alongside the `__main__.py` file . 
This is where your bot token will be loaded from, as well as your database URI (if you're using a database), and most of 
your other settings.

It is recommended to import sample_config and extend the Config class, as this will ensure your config contains all 
defaults set in the sample_config, hence making it easier to upgrade.

An example `config.py` file could be:
```
from cinderella.sample_config import Config


class Development(Config):
    OWNER_ID = "1711642802"# my telegram ID
    OWNER_USERNAME = "Mr_Purushottam_M"  # my telegram username
    API_KEY = "your bot api key"  # my api key, as provided by the botfather
    SQLALCHEMY_DATABASE_URI = 'postgresql://username:password@localhost:5432/database'  # sample db credentials
    MESSAGE_DUMP = '-1234567890' # some group chat that your bot is a member of
    USE_MESSAGE_DUMP = True
    SUDO_USERS = []  # List of id's for users which have sudo access to the bot.
    LOAD = []
    NO_LOAD = ['translation']
```

If you can't have a config.py file (EG on heroku), it is also possible to use environment variables.
The following env variables are supported:
 - `ENV`: Setting this to ANYTHING will enable env variables

 - `TOKEN`: 💫Your bot token, as a string.
 - `OWNER_ID`: 💫An integer of consisting of your owner ID
 - `OWNER_USERNAME`: 💫Your username

 - `DATABASE_URL`: 💫Your database URL
 - `MESSAGE_DUMP`: 💫optional: a chat where your replied saved messages are stored, to stop people deleting their old 
 - `LOAD`: 💫Space separated list of modules you would like to load
 - `NO_LOAD`: 💫 Space separated list of modules you would like NOT to load
 - `WEBHOOK`: 💫Setting this to ANYTHING will enable webhooks when in env mode
 messages
 - `URL`: 💫 The URL your webhook should connect to (only needed for webhook mode)

 - `SUDO_USERS`: 💫A space separated list of user_ids which should be considered sudo users
 - `SUPPORT_USERS`: 💫A space separated list of user_ids which should be considered support users (can gban/ungban,
 nothing else)
 - `WHITELIST_USERS`: 💫A space separated list of user_ids which should be considered whitelisted - they can't be banned.
 - `DONATION_LINK`: 💫Optional: link where you would like to receive donations.
 - `CERT_PATH`: 💫Path to your webhook certificate
 - `PORT`: 💫Port to use for your webhooks
 - `DEL_CMDS`: 💫Whether to delete commands from users which don't have rights to use that command
 - `STRICT_GBAN`: 💫Enforce gbans across new groups as well as old groups. When a gbanned user talks, he will be banned.
 - `WORKERS`: 💫Number of threads to use. 8 is the recommended (and default) amount, but your experience may vary.
 __Note__ that going crazy with more threads wont necessarily speed up your bot, given the large amount of sql data 
 accesses, and the way python asynchronous calls work.
 - `BAN_STICKER`:💫 Which sticker to use when banning people.
 - `ALLOW_EXCL`: 💫Whether to allow using exclamation marks ! for commands as well as /.

### Python dependencies

Install the necessary python dependencies by moving to the project directory and running:

`pip3 install -r requirements.txt`.

This will install all necessary python packages.

### Database

If you wish to use a database-dependent module (eg: locks, notes, userinfo, users, filters, welcomes),
you'll need to have a database installed on your system. I use postgres, so I recommend using it for optimal compatibility.

In the case of postgres, this is how you would set up a the database on a debian/ubuntu system. Other distributions may vary.

- install postgresql:

`sudo apt-get update && sudo apt-get install postgresql`

- change to the postgres user:

`sudo su - postgres`

- create a new database user (change YOUR_USER appropriately):

`createuser -P -s -e YOUR_USER`

This will be followed by you needing to input your password.

- create a new database table:

`createdb -O YOUR_USER YOUR_DB_NAME`

Change YOUR_USER and YOUR_DB_NAME appropriately.

- finally:

`psql YOUR_DB_NAME -h YOUR_HOST YOUR_USER`

This will allow you to connect to your database via your terminal.
By default, YOUR_HOST should be 0.0.0.0:5432.

You should now be able to build your database URI. This will be:

`sqldbtype://username:pw@hostname:port/db_name`

Replace sqldbtype with whichever db youre using (eg postgres, mysql, sqllite, etc)
repeat for your username, password, hostname (localhost?), port (5432?), and db name.



### ༆ 𝚃𝙷𝙰𝙽𝙺𝚂 𝙵𝙾𝚁 𝚅𝙸𝙴𝚆𝙸𝙽𝙶 𝙱𝚄𝚃 𝙺𝙴𝙴𝙿 𝙲𝚁𝙴𝙳𝙸𝚃𝚂



