# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:

Git clone django-orm-project

### STEP 2:

Start myapp and create models and admin

### STEP 3:

Create superuser as admin 

### STEP 4:

Migration of myapp to the server

### STEP 5:

Testing the admin page 

## PROGRAM:

### Models Employee Program:

```
from django.db import models
from django.contrib import admin
# Create your models here.

class Employee(models.Model):
    Eid=models.CharField(primary_key=True,max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('Eid','name','salary','age','email')

```

### Admin Site Program:

```
from django.contrib import admin
from .models import Employee,EmployeeAdmin
# Register your models here.
admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT

### Employee Id Details:

![Employee_details](./img/emp.png)

### Primary Key Error:

![Primary_Key_Error](./img/error.png)

## RESULT:

A Django application to store and retrieve data from a database using Object Relational Mapping(ORM) is Developed.
