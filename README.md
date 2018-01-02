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



## API

### Get Token

`http --auth <user>:<password> POST http://localhost:5000/api/tokens`

### Delete Token

`http DELETE http://localhost:5000/api/tokens "Authorization:Bearer <token>"`

### Get Single User Info
 
`http GET http://localhost:5000/api/users/1 "Authorization:Bearer <token>"`

### Change User Info

`http PUT http://localhost:5000/api/users/2 "about_me=Hi" "Authorization:Bearer <token>"`

### Create User

`http POST http://localhost:5000/api/users username=qmie password=dog email=qmie@example.com "about_me=Hello, my name is Alice" "Authorization:Bearer <token>"`

### Get Followed List

`http GET http://localhost:5000/api/users/1/followed "Authorization:Bearer <token>"`

### Get Followed List

`http GET http://localhost:5000/api/users/1/followers "Authorization:Bearer <token>"`

### Get Users List

`http GET http://localhost:5000/api/users "Authorization:Bearer <token>"`
