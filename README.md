# TooPath v3

TooPath is an API that let you manage tracks and locations related to a device.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

* Install **[python 3.6.1](https://www.python.org/downloads/)**.
* Install **OSGeo4W** following the steps in **[GeoDjango Tutorial](https://docs.djangoproject.com/en/2.0/ref/contrib/gis/tutorial/)** (make sure to install the same bit version of python and OSGeo4W.
* Install **[PyCharm](https://www.jetbrains.com/pycharm/download/)** (optional, recommended for windows users).
 
#### Windows

* Install **[virtualenvwrapper-win](https://pypi.python.org/pypi/virtualenvwrapper-win)** via ```easy_install virtualenvwrapper-win```
* Install **[VirtualBox 5.1](https://www.virtualbox.org/wiki/Downloads)**.
* Install **[Vagrant 2.0.1](https://www.vagrantup.com/downloads.html)**.

#### Linux

* Install **[virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/)** via ```pip install virtualenvwrapper```.
* Install **[PostgreSQL 9.6](https://www.postgresql.org/download/)**.
* Install **[PostGIS 2.3](http://postgis.net/install/)**.

### Environment setup

This environment setup can be done via console and also, via PyCharm console (if you have installed this IDE).
First of all, create a virtual environment:

```
mkvirtualenv [virtual_environment_name]
```

If the virtual environment is not automatically activated, then use:

```
workon [virtual_environment_name]
```

Install all the python requirements:

```
pip install -r requirements.txt
```

As it is recommended on this **[settings tutorial]**, this project has production and local separate settings. To use the local settings setup your **DJANGO_SETTINGS_MODULE** environment variable to ```TooPath3.settings.local```.

For windows users, follow this **[Getting started of Vagrant](https://www.vagrantup.com/intro/getting-started/index.html)** to create a virtual machine with **PostgreSQL** and **PostGIS** (use the versions on [Linux](#Linux) section).

For linux users, you can create the database with the **PostgreSQL** and **PostGIS** previously installed.

Apply all the migrations with:

```
python manage.py migrate
```

#### PyCharm setup

1. Go to  *File>Settings>Project:"name">Project interpreter>Add local*
2. Select **python.exe** from **[virtual_environment_name]** folder
3. Mark *Associate this virtual environment with current project*
4. Configure the settings **INSTALLED_APPS** and **DATABASES** following the steps in **[Configure settings.py](https://docs.djangoproject.com/en/1.11/ref/contrib/gis/tutorial/#configure-settings-py)**

## Running the API

Use ```python manage.py runserver x.x.x.x:aaaa``` where x.x.x.x is the address and aaaa is the port. For local example:

```
python manage.py runserver 127.0.0.1:8080 
```

## Running the tests

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/AlbertWayne/TooPath/tags). 

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
