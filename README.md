# sparta-ruby-api

## Main

Main goal of this repo was to go through the rMVC (routing, Model, Views and Controller) using Sinatra.
We've also used the PostgreSQL database in order to perform CRUD actions in my App (create, read, update and delete.)

Besides the database, an API (Application Performance Interface) was developed in order to have some data back in form of Hash.

Using the JSON gem, it allow us to parse the data from the database into JSON (this can also be parsed into XML or YML if we require the specific gems).

## How to Run the App

1. Make sure you have all the required gems installed, and in your console type:
```
bundle
```

2. In your console type the following (rackup helps our ruby app to rack up all the files and run them in the browser):

```
rackup
```
3. You should see a message in your console saying that your app is being ran in localhost:9292

4. In your browser, type
```
localhost:9292/posts
```

5. You should be able to see a list with random data, edit, delete and add some more if you wish.


## Gems

```
gem install sinatra
gem install sinatra/reloader
gem install pg
gem install json
gem install rack
```

Please note, on the config.ru we have to require the following:
```
require 'sinatra'
require 'sinatra/reloader' if development?
require 'pg'
require 'json'
```


## Setup Instructions - Creating the database
```bash
bundle install
psql -d blog -f seed.sql
```
