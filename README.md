# THC MUSIC HUB https://telegra.ph/file/18b919907ce33599aa30f.jpg [PyTGCalls] [![Mentioned in Awesome Telegram Calls](https://awesome.re/mentioned-badge-flat.svg)](https://github.com/tgcalls/awesome-tgcalls)

THC MUSIC HUB To Play Music With Pytgcalls From Various Sources In Your Group.

<img src="https://telegra.ph/file/18b919907ce33599aa30f.jpg" width="500" height="300">


## Requirements

### Account requirements
- A Telegram account to use as the music bot, **You cannot use regular bot accounts, as they cannot join voice chats. *It must be a user account.***
- API_ID and API_HASH for that account.
- The account must be an admin of the chat, with _Manage Voice Chats_ and _Delete Messages_ permissions.

### Environment requirements
- Linux-based OS. **You cannot run this on Windows natively, Use WSL**
- Python 3.9 or later.
- ffmpeg package, look below for instructions.


## Run (Assuming you have a debian-based distro)



```sh
$ git clone https://github.com/HuntingBots/THCMUSICHUB_tgcall
$ cd Telegram_VC_Bot
$ sudo apt-get install ffmpeg
$ pip3 install -U pip
$ pip3 install -U -r requirements.txt
$ cp sample_config.py config.py
```
Edit **config.py** with your own values.

```sh
$ python3 main.py
```

## Heroku


#### Generate String session [IMPORTANT]

Download this file [generate_string_session.py](https://github.com/HuntingBots/THCMUSICHUB_tgcall/HuntingBots/generate_string_session.py)


```sh
$ pip3 install pyrogram TgCrypto
$ python3 generate_string_session.py
```
Fork this repository and change name of `sample_config.py` to `config.py`
Then you will need get a session string, copy it, then press heroku deploy button.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/HuntingBots/THCMUSICHUB_tgcall/tree/HuntingBots)


Send [commands](https://github.com/HuntingBots/THCMUSICHUB_tgcall/blob/HuntingBots/README.md#commands) to bot to 
play music.


## Docker

```sh
$ git clone https://github.com/HuntingBots/THCMUSICHUB_tgcall && cd THCMUSICHUB_tgcall
$ cp sample.env .env
```
Edit **.env** with your own values.

```sh
$ sudo docker build . -t tgvc-bot
$ sudo docker run tgvc-bot
```
To stop use `CTRL+C`


## Commands
Command | Description
:--- | :---
/help | Show Help Message.
/skip | Skip Any Playing Music.
/play [SONG_NAME] | To Play A Song Using Saavn.<br>Service used can be changed in config (`DEFAULT_SERVICE`).
/play youtube/saavn [SONG_NAME] | To Play A Song Using Specific Service.
/play [with reply to an audio file] | To Play A Song With TG Audio File.
/queue | Check Queue Status.
/delqueue | Deletes Queue List and Playlist.
/playlist [songs name separated by line] | Start Playing Playlist.
/joinvc | Join Voice Chat.
/leavevc | Leave Voice Chat.
/volume [1-200] | Adjust Volume.
/pause | Pause Music.
/resume | Resume Music.


## Note


