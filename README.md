# Rero on Messenger

the multi-purpose discord bot, but yakno on fb.


![Python](https://img.shields.io/badge/python-2.7-blue.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/voqz/rero/master/LICENSE)

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
| fact | tell me a fact | [Offline](https://github.com/voqz/rero/blob/master/data/facts.json) |
| hello | Hi, Rero! | --- |
| help | What can you do? | --- |
| joke | tell me a joke | [Offline](https://github.com/voqz/rero/blob/master/data/jokes.json) |
| lyrics | paradise lyrics | Powered by musiXmatch |
| movie | zootopia movie plot | OMDb API |
| music | songs by one direction | Spotify |
| news | latest news | Powered by NewsAPI |
| quote | random quote | [Offline](https://github.com/voqz/rero/blob/master/data/quotes.json) |
| request | report a bug <br> request a feature | --- |
| time | time in seattle | TimeZoneDB API |
| url | shorten google.com <br> expand http://goo.gl/7aqe | Google URL Shortener |
| video | videos of harry style | YouTube |
| weather | weather in london | Info provided by OpenWeatherMap |
| wiki | wiki html | MediaWiki API |
| xkcd | show a random xkcd comic | [xkcd](https://xkcd.com/json.html) |

More sample queries can be found [here](https://github.com/voqz/rero/tree/master/modules/tests).

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


If you want a public endpoint, use the below button to deploy on Heroku and fill the relevant API keys that you would like to use:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
