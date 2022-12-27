# Cookiecutter Kotsf

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)

Powered by [Cookiecutter](https://github.com/cookiecutter/cookiecutter), Cookiecutter Kotsf is a fork of [Cookiecutter Django](https://github.com/pydanny/cookiecutter-django) optimized for small, quick projects to be deployed on a single server.

## Main Differences

* Single requirements.txt file and .env file for simplicity.
* Deployment scripts and configurations files for nginx, supervisor, and gunicorn.
* Optionally disable socialaccounts in [django-allauth](https://django-allauth.readthedocs.io/en/latest/)
* Database settings use username and password from environment variables to access db. This helps prevent permissions issues on your local machine where the database might end up owned by your user rather than the app user.


## Constraints

* Only maintained 3rd party libraries are used.
* Uses PostgreSQL everywhere (12.13 - 15.1)
* Environment variables for configuration (This won't work with Apache/mod_wsgi).

## Support Cookiecutter-Django!

This fork is made possible because of the excellent work done by the Cookiecutter-Django team. Please support them in their efforts to maintain and improve Cookiecutter Django:

* Daniel Roy Greenfeld, Project Lead [GitHub](https://github.com/pydanny), [Patreon](https://www.patreon.com/danielroygreenfeld): expertise in Django and AWS ELB.

* Nikita Shupeyko, Core Developer [GitHub](https://github.com/webyneter): expertise in Python/Django, hands-on DevOps and frontend experience.

Projects that provide financial support to the maintainers Cookiecutter-Django:
---

[![Two Scoops of Django 3.x](https://cdn.shopify.com/s/files/1/0304/6901/products/Two-Scoops-of-Django-3-Alpha-Cover_540x_26507b15-e489-470b-8a97-02773dd498d1_1080x.jpg)](https://www.feldroy.com/products/two-scoops-of-django-3-x)

Two Scoops of Django 3.x is the best ice cream-themed Django reference in the universe!

pyup
---
[![pyup](https://pyup.io/static/images/logo.png)](https://pyup.io/)

Pyup brings you automated security and dependency updates used by Google and other organizations. Free for open source projects!

## Usage

Let's pretend you want to create a Django project called "redditclone". Rather than using ``startproject``
and then editing the results to include your name, email, and various configuration issues that always get forgotten until the worst possible moment, get [cookiecutter](https://github.com/cookiecutter/cookiecutter) to do all the work.

First, get Cookiecutter. Trust me, it's awesome::

    $ pip install "cookiecutter>=1.7.0"

Now run it against this repo::

    $ cookiecutter https://github.com/ggetzie/cookiecutter-kotsf.git

You'll be prompted for some values. Provide them, then a Django project will be created for you.

**Warning**: After this point, change 'Gabriel Getzie', etc to your own information.

Answer the prompts with your own desired options_. For example:

```
project_name [My Awesome Project]: Reddit Clone
project_slug [reddit_clone]: reddit_clone
description [Behold My Awesome Project!]: A reddit clone
author_name [Gabriel Getzie]: Gabriel Getzie
domain_name [example.com]: redditclone.com
include_www [y]: 
local_port [8001]: 
email [gabriel-getzie@example.com]: admin@redditclone.com
version [0.1.0]: 
Select open_source_license:
1 - MIT
2 - BSD
3 - GPLv3
4 - Apache Software License 2.0
5 - Not open source
Choose from 1, 2, 3, 4, 5 [1]: 1
timezone [UTC]: UTC
windows [n]: n
use_pycharm [n]: n
use_docker [n]: n
use_socialaccount [n]: n
Select postgresql_version:
1 - 15.1
2 - 14.6
3 - 13.9
4 - 12.13
Choose from 1, 2, 3, 4 [1]: 2
Select cloud_provider:
1 - AWS
2 - None
Choose from 1, 2 [1]: 1
Select mail_service:
1 - Amazon SES
2 - Mailgun
3 - Mailjet
4 - Mandrill
5 - Postmark
6 - Sendgrid
7 - SendinBlue
8 - SparkPost
9 - Other SMTP
Choose from 1, 2, 3, 4, 5, 6, 7, 8, 9 [1]: 1
use_async [n]: n
use_drf [n]: n
Select frontend_pipeline:
1 - Gulp
2 - None
3 - Django Compressor
Choose from 1, 2, 3 [1]: 1
use_celery [n]: y
use_mailhog [n]: n
use_sentry [n]: n
use_whitenoise [n]:  n
use_heroku [n]: n
Select ci_tool:
1 - None
2 - Travis
3 - Gitlab
4 - Github
Choose from 1, 2, 3, 4 [1]: 1
keep_local_envs_in_vcs [n]: n
debug [n]: n
 [SUCCESS]: Project initialized, keep up the good work!
```

Enter the project and take a look around::
```
$ cd reddit_clone/
$ ls
```
Create a git repo and push it there::
```
$ git init
$ git add .
$ git commit -m "first awesome commit"
$ git remote add origin git@github.com:ggetzie/redditclone.git
$ git push -u origin master
```
Now take a look at your repo. Don't forget to carefully look at the generated README. Awesome, right?

For local development, see the following:

* [Developing locally](http://cookiecutter-django.readthedocs.io/en/latest/developing-locally.html)
* [Developing locally using docker](http://cookiecutter-django.readthedocs.io/en/latest/developing-locally-docker.html)


## "Your Stuff"

Scattered throughout the Python and HTML of this project are places marked with "your stuff". This is where third-party libraries are to be integrated with your project.


## Code of Conduct

Everyone interacting in the Cookiecutter project's codebases, issue trackers, chat
rooms, and mailing lists is expected to follow the [PyPA Code of Conduct](https://www.pypa.io/en/latest/code-of-conduct/)
