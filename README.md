# Ex02 Django ORM Web Application
# Date:25/10/24
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSPHIP DIAGRAM
![alt text](ormweb/ormapp/erdg.jpg) 
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
~~~
models.py

from django.db import models
from django.contrib import admin
class bankloan(models.Model):
    customer_name=models.CharField(max_length=100,primary_key=True)
    customer_id=models.CharField(max_length=100)
    loan_no=models.IntegerField()
    loan_amount=models.IntegerField()
    email=models.EmailField()
 
class userAdmin(admin.ModelAdmin):
    list_display=('customer_name','customer_id','loan_no','loan_amount','email')
# Create your models here.
~~~
~~~

admin.py

from django.contrib import admin
from .models import bankloan,userAdmin
admin.site.register(bankloan,userAdmin)
~~~







## OUTPUT
![alt text](output1.png)
![alt text](output2.png)
# RESULT
Thus the program for creating a database using ORM hass been executed successfully
