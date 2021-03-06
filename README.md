## Standard Energy Efficiency Data (SEED) Platform™
[![Build Status][travis-img]][travis-url] [![Coverage Status][coveralls-img]][coveralls-url] [![read-the-docs-stable-img]][read-the-docs-stable] [![read-the-docs-latest-img]][read-the-docs-latest]

The SEED Platform is a web-based application that helps organizations easily
manage data on the energy performance of large groups of buildings. Users can
combine data from multiple sources, clean and validate it, and share the
information with others. The software application provides an easy, flexible,
and cost-effective method to improve the quality and availability of data to
help demonstrate the economic and environmental benefits of energy efficiency,
to implement programs, and to target investment activity.

The SEED application is written in Python/Django, with AngularJS, Bootstrap,
and other javascript libraries used for the front-end. The back-end database
is required to be PostgreSQL.

The SEED web application provides both a browser-based interface for users to
upload and manage their building data, as well as a full set of APIs that app
developers can use to access these same data management functions.


### Installation

* Production on Amazon Web Service: See [Installation Notes][production-aws-url]
* Development on Mac OSX: [Installation Notes][development-mac-osx]
* Development using Docker: [Installation Notes][development-docker]

### Starting SEED Platform

In production the following two commands will run the web server (uWSGI) and
the background task manager (Celery) with:

```
bin/start_uwsgi.sh
bin/start_celery.sh
```

In development mode, you can start the web server (uWSGI) and the background
task manager (Celery) with:

```
./manage.py runserver
celery -A seed worker -l info -c 4 --maxtasksperchild 1000 --events
```

### Developer Resources

* Several notes regarding Django and AngularJS integration: See [Developer Resources](...)
* Process monitoring: See [Monitoring](...)

#### Testing

* Running tests: See [Testing Notes](...)

### Copyright
Copyright ©  2014 - 2016, The Regents of the University of California, through
Lawrence Berkeley National Laboratory (subject to receipt of any required
approvals from the U.S. Department of Energy) and contributors. All rights
reserved.


[development-docker]: https://github.com/SEED-platform/seed/wiki/Development-version-of-SEED-on-a-Docker
[development-mac-osx]: https://github.com/SEED-platform/seed/wiki/Development-version-of-SEED-on-a-Mac-OSX
[production-aws-url]: http://www.github.com/seed-platform/seed/wiki/Installation
[read-the-docs-stable]: http://seed-platform.readthedocs.org/en/stable
[read-the-docs-stable-img]: https://readthedocs.org/projects/seed-platform/badge/?version=stable
[read-the-docs-latest]: http://seed-platform.readthedocs.org/en/latest/
[read-the-docs-latest-img]: https://readthedocs.org/projects/seed-platform/badge/?version=latest
[travis-img]: https://travis-ci.org/SEED-platform/seed.svg?branch=develop
[travis-url]: https://travis-ci.org/SEED-platform/seed
[coveralls-img]: https://coveralls.io/repos/SEED-platform/seed/badge.svg
[coveralls-url]: https://coveralls.io/github/SEED-platform/seed
