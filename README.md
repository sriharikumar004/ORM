# Ex02 Django ORM Web Application
## Date: 08/10/25

## AIM
To develop a Django application to store and retrieve data from a Car Inventory Database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
admin.py


from django.contrib import admin
from .models import Car

models.py


from django.db import models

class Car(models.Model):
    make = models.CharField(max_length=100)
    model = models.CharField(max_length=100)
    year = models.IntegerField()
    vin = models.CharField(max_length=17, unique=True)
    price = models.DecimalField(max_digits=10, decimal_places=2)
    color = models.CharField(max_length=50)

    def __str__(self):
        return f"{self.make} {self.model} ({self.year})"


# Register your models here.
admin.site.register(Car)

## OUTPUT

<img width="1910" height="921" alt="Screenshot 2025-10-07 004113" src="https://github.com/user-attachments/assets/afdf79ef-08a1-4a66-aeb2-8ad96052fc27" />


## RESULT
Thus the program for creating car inventory database database using ORM hass been executed successfully
