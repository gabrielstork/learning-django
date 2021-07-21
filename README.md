# learning-django

## Getting Started

Django is an open-source framework that allows us building web applications
with Python.

Fundamental concepts to build an web application:

* An website has two parts, the **front-end** and the **back-end**.

* URL - Uniform Resource Locator (The locator of some resource on the internet, it can be a web page, an image, a video...).

* After client typing the URL, a **request** is sent to the server, the server will process this request and send a **response** back to the client. This data exchange is defined as HTTP (Hypertext Transfer Protocol).

Installing django (it is highly reccomended doing this on a virtual environment).

```sh
pip install django
```

Initiallizing a project called "mysite".

```sh
django-admin startproject mysite
```

This will create a folder called "mysite" at the current directory, that is the core of the application.

Runnig the server on local machine to check if everything went right.

```sh
cd mysite
python manage.py runserver
```

Go to your browser and paste the given link.

![Success](https://github.com/gabrielstork/learning-django/blob/main/images/success.png)

**Done! The environment was created!**

`CTRL + C` to stop the server.