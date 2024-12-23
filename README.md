# Ex02 Django ORM Web Application
## Date: 16-11-2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).



## DESIGN STEPS
![Screenshot 2024-12-14 132012](https://github.com/user-attachments/assets/319ebca7-53fb-4506-a617-551c364ab357)

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
from.models import Loan,LoanAdmin
admin.site.register(Loan,LoanAdmin)

models.py

from django.db import models

from django.contrib import admin
class Loan(models.Model):
   loan_id=models.IntegerField(primary_key=True)
   loan_type=models.CharField(max_length=30)
   loan_amount=models.FloatField()
   cust_acntno=models.IntegerField()
   cust_name=models.CharField(max_length=50)

class LoanAdmin(admin.ModelAdmin):
  list_display=('loan_id','loan_type','loan_amount','cust_acntno','cust_name')  



## OUTPUT
![Screenshot 2024-11-16 150557](https://github.com/user-attachments/assets/2774e950-25a1-4ab4-a1a6-39b81ae89f99)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
