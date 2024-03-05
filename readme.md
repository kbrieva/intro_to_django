## Writing my first Django app

creating folder for django app using git bash

mkdir django ## creates a new directory named "django" in the current location of git bash.

cd django  ## changes the working directory to "django".

python -m django --version   ## checks if django is installed or not, it will show

I use pipenv shell to create an  isolated environment and install django there:

pipenv shell    ## opens a virtual environment called "Pipfile" with python version mentioned in Pipfile. If no such file.

pip install django    ## this command install


## Creating a project

django-admin startproject mysite

This will create mysite directory in your current directory.

Let’s look at what startproject created

mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py


The development server

Let’s verify your Django project works. Change into the outer mysite directory, if you haven’t already, and run the following commands:

py manage.py runserver      ## starts the development web server on http://127.0.0.1:8000/


Creating the Polls app

Now that your environment – a “project” – is set up, you’re set to start doing work.

Each application you write in Django consists of a Python package that follows a certain convention. Django comes with a utility that automatically generates the basic directory structure of an app, so you can focus on writing code rather than creating directories.


Projects vs. apps

What’s the difference between a project and an app? An app is a web application that does something – e.g., a blog system, a database of public records or a small poll app. A project is a collection of configuration and apps for a particular website. A project can contain multiple apps. An app can be in multiple projects.

To create your app, make sure you’re in the same directory as manage.py and type this command:

py manage.py startapp polls

That’ll create a directory polls, which is laid out like this:

polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
