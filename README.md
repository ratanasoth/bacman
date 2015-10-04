# django-bacman #

A simple library that takes a snapshot of a Postgres or MySQL database and uploads it to AWS S3.

## Installation ##

1. Install it

    pip install django-bacman


2. Add to INSTALLED_APPS

    INSTALLED_APPS = (
        ...,
        django-bacman,
    )


3. Run the management scripts

    python manage.py bacman_postgres

or

    python manage.py bacman_mysql


## Settings ##

### DATABASE ###

**DATABASE_URL**

Please add the `DATABASE_URL` variable to your `/etc/environment` or `.pam_environment`

Read more at https://github.com/kennethreitz/dj-database-url


### Amazon Web Services ###

**AWS_ACCESS_KEY_ID**

Please add the `AWS_ACCESS_KEY_ID` variable to your `/etc/environment` or `.pam_environment`

**AWS_SECRET_ACCESS_KEY**

Please add the `AWS_SECRET_ACCESS_KEY` variable to your `/etc/environment` or `.pam_environment`


### BacMan ###

**BACMAN_BUCKET**

Please add the `BACMAN_BUCKET` variable to your `/etc/environment` or `.pam_environment`

**BACMAN_DIRECTORY**
default: /tmp/

**BACMAN_PREFIX**
default (Postgres): pgdump
default (MySQL): mysqldump