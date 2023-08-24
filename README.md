# flask-tut-2023a
Flask app created by following the Flask online tutorial step by step instructions at https://flask.palletsprojects.com/en/2.3.x/tutorial/

This README file is based on the Flask tutorial README located by following the instructions at https://flask.palletsprojects.com/en/2.3.x/contributing/#first-time-setup-using-github-codespaces

This 20230818FlaskTutorial  was a prerequisite for a separate tutorial 2021CreateModelLayer. 

--------------------------------------------------
--------------------------------------------------
#### The steps for starting in a virtual environment are:


In mac terminal, create virtual environment
(this step does not seem to work VSCode terminal) 
Mac/Windows Install instructions can be found here
https://flask.palletsprojects.com/en/2.3.x/installation/

create venv folder (this step is only needed once for each venv)
cd into flask-tut-2023a and run:
$ python ‑m venv venv


In VSCode terminal cd to flask-tut-2023a run
$ source venv/bin/activate

Note: after stopping venv server, this step must be re run to activate venv again

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

Install and update using `pip`_:

.. code-block:: text

    $ pip install -U Flask

.. _pip: https://pip.pypa.io/en/stable/getting-started/


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


Contributing
------------

For guidance on setting up a development environment and how to make a
contribution to Flask, see the `contributing guidelines`_.

.. _contributing guidelines: https://github.com/pallets/flask/blob/main/CONTRIBUTING.rst


Donate
------

The Pallets organization develops and supports Flask and the libraries
it uses. In order to grow the community of contributors and users, and
allow the maintainers to devote more time to the projects, `please
donate today`_.

.. _please donate today: https://palletsprojects.com/donate


Links
-----

-   Documentation: https://flask.palletsprojects.com/
-   Changes: https://flask.palletsprojects.com/changes/
-   PyPI Releases: https://pypi.org/project/Flask/
-   Source Code: https://github.com/pallets/flask/
-   Issue Tracker: https://github.com/pallets/flask/issues/
-   Chat: https://discord.gg/pallets


