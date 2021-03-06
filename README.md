# z14

z14 [zia] is a bot designed to be an extended version of z03 [zoe] from the #inpres chan from maxux.net IRC.

## setup

Install requirements:
```
pip3 install -r requirements.txt
```

Make a local copy of .env:
```
cp .env.sample .env
```

Setup values inside .env according to your environment and settings.

Run z14!
```
python3 z14.py
```

## features

* Reads configuration from .env file
* Assign a default role to any new user
* Assign roles to users based on reactions given to a specific message
* Parse commands

### commands

* .ping - pong
* .km - Will mute Malabar for 5 seconds

## details

You need to configure the bot token in TOKEN

### Default role

New users added to the server will get the role defined in AUTO_ROLE

### Self assigned roles

User can self assign pre-defined roles. They are defined in the env variable
ROLE_EMOJIS as a list of mapping emoji name to role formated as follows:
```
amongus,Among Us;csgo,Counter-Strike Global Offensive
```

The ID of the message users have to react to is given by ROLE_MESSAGE_ID

### km

Based on the original km for kick malabar

* Can not be used more than 3 times a day
* Duration of mute is hardcoded to 5 seconds
