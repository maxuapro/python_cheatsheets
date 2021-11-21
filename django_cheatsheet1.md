## Django cheatsheet

pipenv install Django==3.2.9

django-admin -> command list

django-admin startproject [projectname]
-> creates a folder with the project
cd [projectname]

python manage.py runserver

python manage.py startapp [appname]

add [appname] to INSTALLED_APPS list in settings.py

## Setting up Admin panel
before go to yourwebsite/admin:

```python manage.py migrate```
this sets up a sqlite db

then create a user:

```python manage.py createsuperuser```

login
email sdf@sdf.com
password must be >= 8 chars: like djangotest123


### models
create a model, then:
```python manage.py makemigrations``` then: 
```python manage.py migrate```
! do it everytime we made shanges to our models

also we have to register our model in admin.py file
(we are doing it 1 time)
```py
from django.contrib import admin

# Register your models here.
from .models import Customer
admin.site.register(Customer)
```