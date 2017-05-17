# Rero on Messenger

the multi-purpose discord bot, but yakno on fb.


![Python](https://img.shields.io/badge/python-2.7-blue.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/voqz/reroforfacebook/master/LICENSE)

Messenger is now used by 900 million people every month. With the launch of Send / Receive API, bots are about to [take](http://time.com/4291214/facebook-messenger-bots/) [over](http://www.computerworld.com/article/3055588/social-media/an-army-of-chatbots-will-take-over-facebook-here-s-why.html).


### Modules

Feel free to add to this list by opening an Issue / Pull Request.

| Name | Sample Query | Source (w/ Attribution) |
|:-:|:-:|:-:|
| anime | death note anime | Hummingbird |
| book | anything you want book | Powered by Goodreads |
| bye | goodbye | --- |
| coin | flip a coin | --- |
| currency | usd to eur rate | Fixer.io |
| dice | roll a die | --- |
| dictionary | define comfort | Words API |
| fact | tell me a fact | [Offline](https://github.com/voqz/reroforfacebook/blob/master/data/facts.json) |
| hello | Hi, Rero! | --- |
| help | What can you do? | --- |
| joke | tell me a joke | [Offline](https://github.com/voqz/reroforfacebook/blob/master/data/jokes.json) |
| lyrics | paradise lyrics | Powered by musiXmatch |
| movie | zootopia movie plot | OMDb API |
| music | songs by one direction | Spotify |
| news | latest news | Powered by NewsAPI |
| quote | random quote | [Offline](https://github.com/voqz/reroforfacebook/blob/master/data/quotes.json) |
| request | report a bug <br> request a feature | --- |
| time | time in seattle | TimeZoneDB API |
| url | shorten google.com <br> expand http://goo.gl/7aqe | Google URL Shortener |
| video | videos of harry style | YouTube |
| weather | weather in london | Info provided by OpenWeatherMap |
| wiki | wiki html | MediaWiki API |
| xkcd | show a random xkcd comic | [xkcd](https://xkcd.com/json.html) |

More sample queries can be found [here](https://github.com/voqz/reroforfacebook/tree/master/modules/tests).

### Structure

```sh
├── modules/         # home for various features
├── modules/src/     # code goes here
├── modules/tests/   # tests go here
├── data/            # home for shared data
├── templates/       # for sending structured messages
└── rero.py        # the main bot
```

### Usage

Rero is at your service [here](http://m.me/Rerobot).

### Local Development / Testing

1. Clone this repo.
2. Linux:  
a) Debian (Ubuntu, Linux Mint, etc.): `sudo apt-get install python-dev libffi-dev libssl-dev`  
b) Arch Linux: `sudo pacman -S python2 libffi openssl`  
c) Fedora: `sudo yum install python-devel libffi-devel openssl-devel`  
Windows: These should already be pre-installed in your Python bundle.  
Mac/OS X:  
a) If you install Python using brew, the relevant headers are already installed for you. In other words, you don't need python-devel.  
b) `brew install pkg-config libffi`  
`export PKG_CONFIG_PATH=/usr/local/Cellar/libffi/3.0.13/lib/pkgconfig/` # May change with libffi version  
`pip install cffi`  
c) `brew install libtins`  
3. `pip install -r requirements.txt`
4. `python rero.py`
5. Visit the following URLs to see results:  
`http://localhost:5000/process/?q=<<YOUR_QUERY>>` returns the intent of the query.  
`http://localhost:5000/search/?q=<<YOUR_QUERY>>` returns the search result of the query.

The "process" endpoint returns what module the system classifies your query into, say a dictionary query or a song search, etc. Visit the following URLs to understand the output format:  
`http://localhost:5000/process/?q=tell%20me%20a%20joke`  
`http://localhost:5000/process/?q=time%20in%20seattle`  
`http://localhost:5000/process/?q=convert%2025%20usd%20to%20eur`  
The "search" endpoint returns the actual bot output, that you get when you interact with the bot using that query.

Note that for the search query to work, you have to set your own key (of the module that you want to test) in config.py  

If you want a public endpoint, use the below button to deploy on Heroku and fill the relevant API keys that you would like to use:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
