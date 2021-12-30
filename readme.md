# A simple Url Shortener project
This is a simple Django project implemented to work as an efficient and high speed URL Shortener. 
Async tasks handled using Celery. Furthermore, in order to optimize the response time, this project uses Redis as a cache backend. Some tiny optimizations also performed in Views.

## Table of contents

- [Requirements](#requirements)
- [Getting started](#getting-started)

## Requirements

* [Python3](https://www.python.org/)
* [Django](https://www.djangoproject.com/)
* [Django Rest Framework](https://www.django-rest-framework.org/)
* [Reddis](https://redis.io/)
* [Celery](http://www.celeryproject.org/)

## Project overview

The project is a [Django](https://www.djangoproject.com/start/) application. It serves a URL Shortener using DRF. 

## Getting started

#### Clone the repository

```bash
git clone https://gitlab.com/ehsanmqn/urlshortener
```

#### Prepare the project
```bash
cd url-shortener
virtualenv -p pyhton3 venv
source venv/bin/activate
pip install -r requirements.txt
```

#### Run celery worker

```bash
celery -A UrlShortener worker -B -l info
```

#### Run project

```bash
./manage.py runserver 8000
```

After running the project, it will be accessed through port 8000

Project API document is accessible from [here](https://documenter.getpostman.com/view/5584679/TzJrCf6J)
#### Happy coding!

