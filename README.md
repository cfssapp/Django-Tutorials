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

User.objects.filter(username='Admin')

User.objects.filter(username='Admin').first()
user = User.objects.filter(username='Admin').first()

user
user.id
user.pk

user = User.objects.get(id=2)


Post.objects.all()

post_1 = Post(title='Blog 1', content='First Post Content!', author=user)
post_1.save()

post_2 = Post(title='Blog 2', content='Second Post Content!', author_id=user.id)
post_2.save()

post = Post.objects.first()
post.content
post.date_posted
post.author
post.author.email
post.author.id

.modelname_set

user.post_set.all()

user.post_set.create(title='Blog 3', content='Third Post Content!')

# 06-User-Registration-Form

python manage.py startapp users

pip install django-crispy-forms

# 07-Login-Logout-Authentication

# 08-Profile-And-Images