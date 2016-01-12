# Linux Configuration Project

### The application can be accessed [here][1] until Udacity course is over.

## Table of contents
- [Summary](#summary)
- [Links](#links)
- [Summary of Changes](#summary-of-changes)
- [Extras](#extras)
- [References](#references)

## Summary
In this project, I prepared a Linux virtual machine by installing and configuring web and database servers, sercured it from a number of attacks, then used it to host a web application.  The web server is running on a temporary Amazon AWS instance provided by Udacity.  That instance will be canceled shortly after the course is over.

## Links
- IP Address: 52.35.80.19
- SSH Port: 2200
- Application URL: http://ec2-52-35-80-19.us-west-2.compute.amazonaws.com

## Summary of Changes
### Installed Software:
alembic (0.7.7), argparse (1.2.1), astroid (1.3.8), blinker (1.4), dominate (2.1.12),
enum34 (1.0.4), Flask (0.10.1), Flask-DebugToolbar (0.10.0), Flask-Login (0.2.11),
Flask-Migrate (1.5.0), Flask-Moment (0.5.1), Flask-Rauth (0.3.2), Flask-Script (2.0.5),
Flask-SQLAlchemy (2.0), Flask-Testing (0.4.2), Flask-WTF (0.12), idna (2.0),
ipaddress (1.0.14), itsdangerous (0.24), Jinja2 (2.8), logilab-common (1.0.2), Mako (1.0.1),
MarkupSafe (0.23), nose (1.3.7), pip (1.5.4), psycopg2 (2.6.1), pyasn1 (0.1.8),
pycparser (2.14), pylint (1.4.4), rauth (0.7.1), requests (2.7.0), setuptools (2.2),
six (1.9.0), SQLAlchemy (1.0.8), Werkzeug (0.10.4), wheel (0.24.0), wsgiref (0.1.2),
WTForms (2.0.2)

### Changes
* Created a new user named grader
* Made grader a sudoer
* Updated all currently installed packages
* Changed the SSH port from 22 to 2200
* Configured the UFW (Firewall) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)
* Configured the local timezone to UTC
* Installed and configured Apache to serve a Python mod_wsgi application
* Installed and configured PostgreSQL:
* Dissallowed remote password ssh by root
* created a new catalog grader user roles with limited permissions to database.
* Deployed the catalog application

[1]: http://ec2-52-35-80-19.us-west-2.compute.amazonaws.com