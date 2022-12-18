# Django ORM Web Application

## AIM :
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram :



## DESIGN STEPS :

### STEP 1 
```
   Create a django project using "django-admin startproject studentproject"

   We will get a new folder
   
   Now go into student project folder using "cd studentproject"

   create a new folder inside studentproject using "python3 manage. py startapp stueligibility "

   In settings .py allow host and add the folder "stueligibility" in installed apps.

   Save the file

   And in terminal : "python3 manage. py runserver 0:80"
```

### STEP 2
```
   Open new terminal

   change directory to studentproject "Cd studentproject"

   make migrations using "python3 manage.py makemigrations"

                         "python3 manage.py migrate"

   create a super user "python3 manage.py createsuperuser"

   create username ,email id and password 

   python3 manage.py runserver 0:80

   log in to django administration using username and password
```

### STEP 3

```
   Go to stueligibility - models.py
   
   code the program and save it

   Go to admin .py 

   code and save it

   Now make migrations 
   
   Make sure we are inside studentproject folder and now run the application using "python3 manage.py runserver 0:80"

   Now search the url of the website in chrome,log in and create tables

```
## PROGRAM :

### In Models. py :
```
from django.db import models
from django.contrib import admin
class Student (models.Model):
    referencenumber = models.CharField(max_length=8,primary_key=True)
    name = models.IntegerField()
    dateofbirth = models.DateField()
    email = models.EmailField()
    subjectcode = models.CharField(max_length=4)
    attendance = models.FloatField()
    eligibility = models.CharField(max_length=20)
class StudentAdmin (admin.ModelAdmin):
    list_display = ('referencenumber','name','email','subjectcode','attendance','eligibility')

```
### In Admin. py :

```
from django.contrib import admin
from .models import Student,StudentAdmin

admin.site.register(Student,StudentAdmin)
```

## OUTPUT :




## RESULT :
Created a stueligibility table with Django application to store and retrieve data from a database using Object Relational Mapping(ORM).
