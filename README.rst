Cookiecutter Kotsf
===================

.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :alt: Code style: black
    :target: https://github.com/ambv/black

Powered by `Cookiecutter <https://github.com/cookiecutter/cookiecutter>`_, Cookiecutter Kotsf is a fork of `Cookiecutter Django <https://github.com/pydanny/cookiecutter-django>`_

Main Differences
----------------

* Single requirements.txt file and .env file for simplicity.
* Deployment scripts and configurations files for nginx, supervisor, and gunicorn.
* Optionally disable socialaccounts in `django-allauth <https://django-allauth.readthedocs.io/en/latest/>`_
* Database settings use username and password from environment variables to access db. This helps prevent permissions issues on your local machine where the database might end up owned by your user rather than the app user.


Constraints
-----------

* Only maintained 3rd party libraries are used.
* Uses PostgreSQL everywhere (12.13 - 15.1)
* Environment variables for configuration (This won't work with Apache/mod_wsgi).

Support Cookiecutter-Django!
----------------------------

This fork is made possible because of the excellent work done by the Cookiecutter-Django team. Please support them in their efforts to maintain and improve Cookiecutter Django:

* Daniel Roy Greenfeld, Project Lead (`GitHub <https://github.com/pydanny>`_, `Patreon <https://www.patreon.com/danielroygreenfeld>`_): expertise in Django and AWS ELB.

* Nikita Shupeyko, Core Developer (`GitHub <https://github.com/webyneter>`_): expertise in Python/Django, hands-on DevOps and frontend experience.

Projects that provide financial support to the maintainers Cookiecutter-Django:

~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: https://cdn.shopify.com/s/files/1/0304/6901/products/Two-Scoops-of-Django-3-Alpha-Cover_540x_26507b15-e489-470b-8a97-02773dd498d1_1080x.jpg
   :name: Two Scoops of Django 3.x
   :align: center
   :alt: Two Scoops of Django
   :target: https://www.feldroy.com/products//two-scoops-of-django-3-x

Two Scoops of Django 3.x is the best ice cream-themed Django reference in the universe!

pyup
~~~~~~~~~~~~~~~~~~

.. image:: https://pyup.io/static/images/logo.png
   :name: pyup
   :align: center
   :alt: pyup
   :target: https://pyup.io/

Pyup brings you automated security and dependency updates used by Google and other organizations. Free for open source projects!

Usage
------

Let's pretend you want to create a Django project called "redditclone". Rather than using ``startproject``
and then editing the results to include your name, email, and various configuration issues that always get forgotten until the worst possible moment, get cookiecutter_ to do all the work.

First, get Cookiecutter. Trust me, it's awesome::

    $ pip install "cookiecutter>=1.7.0"

Now run it against this repo::

    $ cookiecutter https://github.com/pydanny/cookiecutter-django

You'll be prompted for some values. Provide them, then a Django project will be created for you.

**Warning**: After this point, change 'Daniel Greenfeld', 'pydanny', etc to your own information.

Answer the prompts with your own desired options_. For example::

    Cloning into 'cookiecutter-django'...
    remote: Counting objects: 550, done.
    remote: Compressing objects: 100% (310/310), done.
    remote: Total 550 (delta 283), reused 479 (delta 222)
    Receiving objects: 100% (550/550), 127.66 KiB | 58 KiB/s, done.
    Resolving deltas: 100% (283/283), done.
    project_name [Project Name]: Reddit Clone
    project_slug [reddit_clone]: reddit
    author_name [Daniel Roy Greenfeld]: Daniel Greenfeld
    email [you@example.com]: pydanny@gmail.com
    description [Behold My Awesome Project!]: A reddit clone.
    domain_name [example.com]: myreddit.com
    version [0.1.0]: 0.0.1
    timezone [UTC]: America/Los_Angeles
    use_whitenoise [n]: n
    use_celery [n]: y
    use_mailhog [n]: n
    use_sentry [n]: y
    use_pycharm [n]: y
    windows [n]: n
    use_docker [n]: n
    use_heroku [n]: y
    use_compressor [n]: y
    Select postgresql_version:
    1 - 13.2
    2 - 12.6
    3 - 11.11
    4 - 10.16
    Choose from 1, 2, 3, 4, 5 [1]: 1
    Select js_task_runner:
    1 - None
    2 - Gulp
    Choose from 1, 2 [1]: 1
    Select cloud_provider:
    1 - AWS
    2 - GCP
    3 - None
    Choose from 1, 2, 3 [1]: 1
    custom_bootstrap_compilation [n]: n
    Select open_source_license:
    1 - MIT
    2 - BSD
    3 - GPLv3
    4 - Apache Software License 2.0
    5 - Not open source
    Choose from 1, 2, 3, 4, 5 [1]: 1
    keep_local_envs_in_vcs [y]: y
    debug[n]: n

Enter the project and take a look around::

    $ cd reddit/
    $ ls

Create a git repo and push it there::

    $ git init
    $ git add .
    $ git commit -m "first awesome commit"
    $ git remote add origin git@github.com:pydanny/redditclone.git
    $ git push -u origin master

Now take a look at your repo. Don't forget to carefully look at the generated README. Awesome, right?

For local development, see the following:

* `Developing locally`_
* `Developing locally using docker`_

.. _options: http://cookiecutter-django.readthedocs.io/en/latest/project-generation-options.html
.. _`Developing locally`: http://cookiecutter-django.readthedocs.io/en/latest/developing-locally.html
.. _`Developing locally using docker`: http://cookiecutter-django.readthedocs.io/en/latest/developing-locally-docker.html

Community
-----------

* Have questions? **Before you ask questions anywhere else**, please post your question on `Stack Overflow`_ under the *cookiecutter-django* tag. We check there periodically for questions.
* If you think you found a bug or want to request a feature, please open an issue_.
* For anything else, you can chat with us on `Slack`_.

.. _`Stack Overflow`: http://stackoverflow.com/questions/tagged/cookiecutter-django
.. _`issue`: https://github.com/pydanny/cookiecutter-django/issues
.. _`Slack`: https://join.slack.com/t/cookie-cutter/shared_invite/enQtNzI0Mzg5NjE5Nzk5LTRlYWI2YTZhYmQ4YmU1Y2Q2NmE1ZjkwOGM0NDQyNTIwY2M4ZTgyNDVkNjMxMDdhZGI5ZGE5YmJjM2M3ODJlY2U


"Your Stuff"
-------------

Scattered throughout the Python and HTML of this project are places marked with "your stuff". This is where third-party libraries are to be integrated with your project.


Code of Conduct
---------------

Everyone interacting in the Cookiecutter project's codebases, issue trackers, chat
rooms, and mailing lists is expected to follow the `PyPA Code of Conduct`_.


.. _`PyPA Code of Conduct`: https://www.pypa.io/en/latest/code-of-conduct/
