# linux-server-configuration

This readme covers linux server configuration process for the final project of Udacity's Full Stack Nanodegree.

IP address: 18.217.92.66

SSH Port: 2200

URL: http://ec2-18-217-92-66.us-east-2.compute.amazonaws.com/

## Accessing the Item Catalog App

To access the site, simply visit `http://18.217.92.66` or `http://ec2-18-217-92-66.us-east-2.compute.amazonaws.com/` in your preferred browser. The app utilizes Google oauth, so a google account is necessary to create/update/delete within the app.

## Accessing as `grader`

`ssh grader@18.217.92.66 -p 2200 -i <location of private key pasted in "Notes to Reviewer">`


## Server Configurations and Installations

Configurations:

    -Update packages

    -Disable remote login to root

    -Change SSH Port from 22 to 2200

    -Configure UFW to only allow connections via SSH (port 2200), HTTP (port 80), and NTP (port 123)

    -Create new user `grader`

    -Grant `sudo` permission to `grader`

    -Create SSH key pair via `ssh-keygen` for `grader` and add public key to server

    -Set timezone to UTC

    -Install Apache

    -Install/Enable mod_wsgi applications for Python3

    -Install/setup PostgreSQL DB

    -Create postgresql `catalog` user with limited permissions

    -Confirm remote connections are not enabled

    -Install git for catalog app deployment

    -Clone item catalog project from github

    -Add catalog.conf file to serve app

    -Install py dependencies view virtualenv

    -Modify project to work with PostgreSQL instead of SQLite, and function as a wsgi app

Installations:

    -apache2

    -libapache2-mod-wsgi-py3

    -flask (via pip/python3)

    -sqlalchemy (via pip/python3)

    -oauth2client (via pip/python3)

    -virtualenv (via pip/python3)
    
    -ntp

## Resources

During the configuration process I utilized Udacity's forums, as well as documentation/direct tutorials (i.e. apache, ubuntu, digitalocean).