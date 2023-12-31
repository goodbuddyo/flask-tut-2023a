# flask-tut-2023a
Flask app from the Flask online tutorial step by step instructions at https://flask.palletsprojects.com/en/2.3.x/tutorial/

This README file is based on the instructions at https://flask.palletsprojects.com/en/2.3.x/contributing/#first-time-setup-using-github-codespaces


--------------------------------------------------
--------------------------------------------------
#### The steps for starting in a virtual environment are:


In mac terminal, create virtual environment
(this step does not seem to work VSCode terminal) 
Mac/Windows Install instructions can be found here
https://flask.palletsprojects.com/en/2.3.x/installation/

create venv folder (this step is only needed once for each venv)
cd into flask-tut-2023a and run:
$ python ‑m venv .venv


In VSCode terminal cd to flask-tut-2023a run
$ source .venv/bin/activate

Note: after stopping venv server, this step must be re run to activate venv again
$ source .venv/bin/activate

Install Flask  (this step is only needed once for each venv)
$ pip install Flask

Before running the app, initialize the DB
$ flask --app flaskr init-db

Run the app
$ flask --app flaskr run --debug

View app at http://127.0.0.1:5000/


To stop dev server, use steps necessary for your system
for some macs Ctrl + D 
or 
lsof -i tcp:5000 
[get pid]
kill -9 pid
close all terminals

--------------------------------------------------
--------------------------------------------------

Flask
=====

Flask is a lightweight `WSGI`_ web application framework. It is designed
to make getting started quick and easy, with the ability to scale up to
complex applications. It began as a simple wrapper around `Werkzeug`_
and `Jinja`_ and has become one of the most popular Python web
application frameworks.

Flask offers suggestions, but doesn't enforce any dependencies or
project layout. It is up to the developer to choose the tools and
libraries they want to use. There are many extensions provided by the
community that make adding new functionality easy.

.. _WSGI: https://wsgi.readthedocs.io/
.. _Werkzeug: https://werkzeug.palletsprojects.com/
.. _Jinja: https://jinja.palletsprojects.com/


Installing
----------
$ cd flask-tut-2023a
$ python3 -m venv venv   #this creates a venv folder
$ source venv/bin/activate  # will now see (venv) in the terminal


Install and update using `pip`_:

.. code-block:: text

(venv) $ pip install -U Flask

.. _pip: https://pip.pypa.io/en/stable/getting-started/


Starting
----------
cd to folder
$ source venv/bin/activate
$ flask --app flaskr run --debug
http://127.0.0.1:5000/


A Simple Example
----------------

.. code-block:: python

    # save this as app.py
    from flask import Flask

    app = Flask(__name__)

    @app.route("/")
    def hello():
        return "Hello, World!"

.. code-block:: text

    $ flask run
      * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)



Links
-----

-   Documentation: https://flask.palletsprojects.com/
-   Changes: https://flask.palletsprojects.com/changes/
-   PyPI Releases: https://pypi.org/project/Flask/
-   Source Code: https://github.com/pallets/flask/
-   Issue Tracker: https://github.com/pallets/flask/issues/
-   Chat: https://discord.gg/pallets


Notes:
This 20230818FlaskTutorial  was a recommended prerequisite for a separate tutorial 2021CreateModelLayer. 
Notes: /pluralsight/Python/Flask_a/FlaskDocumentation/20230818a_FlaskTutorial\
/repos/python/flask-tut-2023a
https://github.com/goodbuddyo/flask-tut-2023a

### --------------------
### Setup Notes

clone from github
https://github.com/pallets/flask/tree/main/examples/tutorial
see /repos/python/flask-tut-2023a
cd ... flask-tut-2023a
$ python -m venv venv      #this creates a venv folder
$ source venv/bin/activate     # will now see (venv) in the terminal
(venv) $ pip install Flask     # if not already installed in venv

To start the server
Run the app
	$ flask --app flaskr run --debug

To stop the server, run
  lsof -i tcp:5000  >  [get the PID]  > kill -9 PID

View in browser
	http://127.0.0.1:5000/hello


### notes --------------------

$ mkdir flaskr
Create file /flaskr/__init__.py 
  def create_app(test_config=None):
    ....
  return app    
Create db file 	flaskr/db.py
  def get_db():
    ...
    return g.db
  def close_db(e=None):
Create flaskr/schema.sql
  CREATE TABLE user (
    ...
  CREATE TABLE post (
    ...
