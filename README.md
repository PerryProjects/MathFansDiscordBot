# MathFansJuggler

MathFanJuggler is a Python based Discord Bot to help with streaming/lecturing during COVID-19

## Installation
Create a server
If you don't already have a server, create one free one at https://discordapp.com. Simply log in, and then click the plus sign on the left side of the main window to create a new server.

Create an app
Go to https://discordapp.com/developers/applications/me and create a new app. On your app detail page, save the Client ID. You will need it later to authorize your bot for your server.

Create a bot account for your app
After creating app, on the app details page, scroll down to the section named bot, and create a bot user. **Save the token**, you will need it later to run the bot.

Authorize the bot for your server
Visit the URL https://discordapp.com/oauth2/authorize?client_id=XXXXXXXXXXXX&scope=bot but replace XXXX with your app client ID. Choose the server you want to add it to and select authorize.

Install the python package discord.py
Run pip install from your system terminal/shell/command prompt.

```bash
python -m pip install discord.py
```

Download the compressed ZIP file [here](https://github.com/PerryProjects/MathFansJuggler/archive/master.zip) and unzip into another folder.

Instructions Sourced from: [Dungeon Dev](https://www.devdungeon.com/content/make-discord-bot-python) See link for more details

## Usage
To start your instance of the bot some changes are needed to the main python file.

Open mathfansjuggler.py with a text editor such as notepad, notepad++, etc.

On download, lines 9-12 should look like:
```python
# Change Per Server Deployment
token = 'bot_token'
instructor = 307362705684299777
server_name = 'Test Server'
```

You will need to change these values to:
1. Your personal **token** found when you created the bot account on discord (see Installation)
2. Your personal **client_id** which can be found by right clicking your username in any discord chat and selecting 'copy id' at the bottom
3. The name of the server where you would like to use this bot

The resulting code block should look something like this:
```python
# Change Per Server Deployment
token = 'D43f5y0ahjqew82jZ4NViEr2YafMKhue'
instructor = 307362705684299777
server_name = 'My Test Server'
```

Once you have verified that the submitted information is correct, save and exit. Then run the attached 'run.bat'

## Commands

For the Student:
Command | Function
------------ | -------------
**!attendance {student name}** | logs the student to the attendance log
**!talk** | adds the user to the voice queue
**!done** | removes the user from the voice queue
**!queue** | shows current queue to ask questions
**!poll** | creates a reaction poll with format [!poll <question>? <option1>:<option2>]

For the Instructor:
Command | Function
------------ | -------------
**!start** | start class, will mute users in voice chat
**!end** | ends class, will unmutes all users in voice chat
**!qauto** | changes questions to cycle automatically
**!qsingle** | changes questions to cycle one at a time
**!next** | cycles to the next student in line
**!changeinstructor {instructor_id}** | changes the current instructor to a new instructor

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)