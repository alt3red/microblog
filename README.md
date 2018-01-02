# Welcome to Microblog

This is an example application using Flask, written by Miguel Grinberg.

## Prerequisites

### Mac

`brew install elasticsearch`

`brew install redis`

## Config

You will need a .env file with the following:

ex:

SECRET_KEY=a-really-long-and-unique-key-that-nobody-knows
MAIL_SERVER=localhost
MAIL_PORT=25
MS_TRANSLATOR_KEY=<your-translator-key-here>

## Run

### Mac

`redis-server /usr/local/etc/redis.conf`

`rq worker microblog-tasks`

`elasticsearch`

`./localmail.sh`

`python3 -m venv venv`

`source venv/bin/activate`

`pip install -r requirements.txt`

`export FLASK_APP=microblog.py`

`flask run`