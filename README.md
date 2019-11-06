# 01-Getting-Started

pip install django

python -m django --version

django-admin

django-admin startproject django_project .

python manage.py runserver


# 02-Application-And-Routes

python manage.py startapp blog


# 03-Templates

# 04-Admin-Page

python manage.py createsuperuser

python manage.py makemigrations

python manage.py migrate

# 05-Database-Models

python manage.py sqlmigrate blog 0001

python manage.py shell

from blog.models import Post

from django.contrib.auth.models import User

User.objects.all()

User.objects.first()