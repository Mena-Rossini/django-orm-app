# Django ORM Web Application

## AIM :
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram :

![ormdiagram](https://user-images.githubusercontent.com/102855266/213182286-3baae3b4-604c-442c-af12-6a3ba17b33cc.jpg)



## DESIGN STEPS :

### STEP 1 :
Create a django project and start app

### STEP 2 : 
Create Superuser

### STEP 3
Runserver and create tables

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
### terminal :
![ormcode](https://user-images.githubusercontent.com/102855266/213182194-13df0f8f-77c7-42fa-9852-a074a63b1202.jpg)



### webpage:


![orm webpage](https://user-images.githubusercontent.com/102855266/213182235-81d7fe45-7e9c-4f55-b978-b1c3388cb868.jpg)


## RESULT :
Created a stueligibility table with Django application to store and retrieve data from a database using Object Relational Mapping(ORM).
