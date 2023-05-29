# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Create a new Django project using "django-admin startproject",get into the project's terminal and use "python3 manage.py startapp hospitalproject" command.

### STEP 2:
Define a model for the Hospitalapp in the models.py and allow host access and add the app name under the installed apps in settings.py

### STEP 3:
Register the models with the Django admin site. In admin.py under app folder, register the models with Django admin site.


## PROGRAM
```python
Models.py

from django.db import models
from django.contrib import admin
# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(primary_key=20,max_length=4,help_text='reference number')
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    phone=models.IntegerField()
class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','phone')

Admin.py
from django.contrib import admin
from .models import Student,StudentAdmin

admin.site.register(Student,StudentAdmin)
```



## OUTPUT
![](/Screenshot%202023-05-29%20091726.png)
![](/Screenshot%202023-05-29%20092637.png)


## RESULT
Thus a Django application to store and retrieve data from a database using Object Relational Mapping(ORM) is developed.