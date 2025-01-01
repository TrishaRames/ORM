# Ex02 Django ORM Web Application
## Date:26-10-24 

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM
![Screenshot 2024-10-26 210306 - Copy](https://github.com/user-attachments/assets/5de94af8-0e1e-49ec-a603-2f188ca61db2)



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
```
from django.db import models
from django.contrib import admin
class bankloan(models.Model):

  Name=models.CharField(max_length=100)
  Accno=models.IntegerField(primary_key="accno")
  Phoneno=models.IntegerField()
  Startingdate=models.DateField()
  Email=models.EmailField()
  Amount=models.IntegerField()
  Interest=models.FloatField()
  Endingdate=models.DateField()
class bankloanAdmin(admin.ModelAdmin): 
  list_display=('Name','Accno','Phoneno','Startingdate','Email','Amount','Interest','Endingdate')


from django.contrib import admin
from .models import bankloan,bankloanAdmin
admin.site.register(bankloan,bankloanAdmin)
```



## OUTPUT

![Screenshot (60)](https://github.com/user-attachments/assets/bd53158d-d517-4774-92aa-060f6028da43)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
