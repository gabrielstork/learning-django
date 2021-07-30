# learning-django

A quick read django tutorial made by me, to test my knowledge.

## Getting Started

Django is an open-source framework that allow us building web applications with Python.

Before all, it is important to know some fundamental concepts of how websites actually work:

* A website has two parts, the **front-end** (the visual and interactive part, can be called as **client-side**, since is the part that the user interacts with, and it is normally made of HTML + CSS + JavaScript) and the **back-end** (the part that is not accessible to users and where everything actually happens, it consists basically of a server, a database and multiple applications, can be called as **server-side**).

* URL - Uniform Resource Locator (The locator of some resource on the internet, it can be a web page, an image, a video, a PDF...).

* After client typing the URL, a **request** is sent to the server. The server will process the request and send a **response** back to the client. This data exchange is defined as HTTP (Hypertext Transfer Protocol).

![HTTP](https://github.com/gabrielstork/learning-django/blob/main/images/http.png)

Installing django (it is highly reccomended doing this on a virtual environment).

```sh
pip install django
```

Initiallizing a project called "mysite".

```sh
django-admin startproject mysite
```

This will create a folder called "mysite" (the project itself) at the current directory, and inside it, another folder called "mysite", that is the core of the project.

Runnig the server on local machine to check if everything went right.

```sh
cd mysite
python manage.py runserver
```

Note that a type of warning appears, you don't need to worry about it now, it is just telling that the applications of the project were not migrated. You will see it better later.

```text
You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
```

Go to your browser and paste the given link.

![Success](https://github.com/gabrielstork/learning-django/blob/main/images/success.png)

**Done! Your project is working!**

`CTRL + C` to stop the server.

Now, that the project was created and it is properly working, you need to create your first application.

Here, I will create an application called `main`.

```sh
python manage.py startapp main
```

After creating the application, you need to connect it to the project. `settings.py` is the settings from the django project, and you must add in there your recently created application.

First you will see this (the default apps on the project, you can delete the ones that are not useful to your case, but as it is just a tutorial, let's keep them):

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```

So, to add your app, you simply need to append it to the list.

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'main.apps.MainConfig',
]
```

To better understand the `main.apps.MainConfig`, you can check on your application folder the `apps.py` and the function on it.

You can run the server again and check if everything went ok.

Now that both are connected, we can move on to URLs.
