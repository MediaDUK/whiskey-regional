# Whiskey Regional - Whiskey By Regions

> A fullstack project built with python, flask (Jinja2 views), PostgreSQL, and Google OAuth 2.0.

## What's inside

In the repo you'll find the following directories and files.

| File/Folder          | Provides                                       |
|----------------------|------------------------------------------------|
| README.md            | how to instructions                            |
| app.py               | launch app                                     |
| client_secrects.js   | see set up OAuth 2.0                           |
| create_db.py         | schema SQLAlchemy classes                      |
| load_whiskey.py      | dummy data to insert                           |
| /static              | JS, CSS, Fonts, images                         |
| /templates           | html views                                     |
| /uploads             | directory for user uploads                     |

## Requirements / Dependencies

Local prototyping setup for Mac OS X (10.11.x).
Install python 2 and PostgreSQL however you like.
I like [homebrew](http://brew.sh/) package manager.

### Install [python>=2.7.12](https://www.python.org/download/releases/2.7/) and [PostgreSQL>=9.6.1](https://www.postgresql.org/docs/9.6/static/index.html)

```bash
[user@machine/~]
$ brew install python PostgreSQL
```

### Install [flask>=0.11.1](http://flask.pocoo.org/docs/0.11/), [sqlalchemy>=1.1](http://docs.sqlalchemy.org/en/latest/intro.html), [Flask-SeaSurf>=0.2.2](https://flask-seasurf.readthedocs.io/en/latest/), [oauth2client](https://github.com/google/oauth2client), [requests](http://docs.python-requests.org/en/master/user/install/)

```bash
[user@machine/~]
$ pip install Flask SQLAlchemy flask-seasurf oauth2client requests
```

## Getting Started

### Clone & enter repo

```bash
git clone https://github.com/MediaDUK/whiskey-regional.git && cd _$
```

### Set up [OAuth 2.0](https://support.google.com/googleapi/answer/6158849?hl=en&ref_topic=7013279)

Python specific implementation located [here](https://developers.google.com/api-client-library/python/guide/aaa_oauth)
Once OAuth is enabled download client_secrets.json from  API console after and
place in root directory. App cannot insert into local database without user
authentication via google account.

### Build Database

```bash
python create_db.py
```

### Load Some Whiskey

```bash
python load_whiskey.py
```

### Run Application

```bash
python app.py
```

### Open browser to [http://localhost:8000/](http://localhost:8000/)

## Viewing App

### Click top right "Sign In" Button

sign in via google account(email password not implemented yet)--you will be redirected to home page and '+ Whiskey' button
will be available after user verification.

## JSON & XML Web Services:

Visit the following endpoints to return the specified data

## JSON

### [http://localhost:8000/brands/JSON](http://localhost:8000/brands/JSON)

> _return all brands_

### [http://localhost:8000/regions/JSON](http://localhost:8000/regions/JSON)

> _return all regions_

### [http://localhost:8000/brands/<int:id>/JSON](http://localhost:8000/brands/<int:id>/JSON)

> _return single brand_

#### [http://localhost:8000/regions/<int:id>/JSON](http://localhost:8000/regions/<int:id>/JSON)

> _return single region_

## XML (eh, why not?)

### [http://localhost:8000/brands/XML](http://localhost:8000/brands/XML)

> _return all brands_

### [http://localhost:8000/regions/XML](http://localhost:8000/regions/XML)

> _return all regions_
