Flask-Imagine-GoogleAdapter
============

[![Author](https://img.shields.io/badge/author-Kronas-blue.svg)](https://github.com/kronas)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/kronas/Flask-Imagine/master/LICENSE)
[![Documentation Status](https://readthedocs.org/projects/flask-imagine/badge/?version=latest)](http://flask-imagine.readthedocs.org/en/latest/?badge=latest)

Google Cloud Storage adapter for [Flask-Imagine](https://github.com/FlaskGuys/Flask-Imagine) extension.

Installation
------
```
$ pip install Flask-Imagine-GoogleAdapter
```

Configuration example
------
```
from flask import Flask
from flask.ext.imagine import Imagine
from flask.ext.flask_imagine_google_adapter import FlaskImagineGoogleAdapter

app = Flask(__name__)

app.config['IMAGINE_ADAPTERS'] = {
    'gcs': FlaskImagineGoogleCloudAdapter
}

app.config['IMAGINE_ADAPTER'] = {
    'name': 'gcs',
    'client_id': 'your_access_key',
    'client_secret': 'your_secret_key',
    'bucket_name': 'your_bucket_name',
    'domain': 'domain.tld'      # Domain name for using static website hosting
    'schema': 'https'
}

# ... Another configuration options

# Init extension
imagine = Imagine(app)
#  or 
imagine = Imagine()
imagine.init_app(app)
```
