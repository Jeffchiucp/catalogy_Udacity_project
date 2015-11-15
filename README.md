# udacity_fullstack_project3
udacity Full Stack Web Developer Nanodegree Project 3 - Item Catalog

##Files
* application.py -- python script with flask main application
* catalog.db -- sqlite database for item catalog
* database_setup.py -- pathon script for sqlalchemy database schema
* addData.py -- python script to polulate database with sample data
* static/styles.css -- css style for all views
* templates/additem.html -- template for item add view
* templates/catalog.html -- template for catalog and category overview
* templates/deleteitem.html -- template for item delete view
* templates/edititem.html -- template for item edit view
* templates/item.html -- template for item view
* templates/header.html -- header for all views
* templates/footer.html -- footer for all views

## Requirements

* python
* [flask](http://flask.pocoo.org) 
* [sqlalchemy](http://www.sqlalchemy.org)
* [SeaSurf](https://flask-seasurf.readthedocs.org)
* [GitHub-Flask](https://github-flask.readthedocs.org/en/latest/)

Setup

for GitHub OAuth the Client ID and Client Secret have to be changed in application.py:

app.config['GITHUB_CLIENT_ID'] = 'XXX'
app.config['GITHUB_CLIENT_SECRET'] = 'YYY'
for session management you should change the secret key of the app:
app_secret = 'ZZZ'

the callback url should be something like https://jeffchiu605/login/callback
We need to make sure all our callback urls match. 
Our authorised endpoint that the url is: /github-callback, and because we are testing on localhost we'll need to include that too:
github_callback_url = "http://localhost:5000/github-callback"

and can be configured in the head of application.py:

In our github account we need to make sure the "Authorization callback URL" also matches this url:

http://localhost:5000/github-callback

To reset database.
rm catalog.db
python addData.py

Need to install in order to run the application.py
$pip install GitHub-Flask
$pip install flask-seasurf