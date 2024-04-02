# Ex03 Time Table
## Date:02.04.2024

## AIM
To write a html webpage page to display your slot timetable.

## ALGORITHM
### STEP 1
Create a Django-admin Interface.

### STEP 2
Create a static folder and inert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html.

### STEP 4
Add header row using ```<th>``` tag.

### STEP 5
Add your timetable using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM
### Home.html:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Time Table</title>
    {% load static %}
    <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>
    <p>SLOT TIME TABLE - AISHWARYA T M (21500105)</p>
    <table border="1">
        <tr class="row">
            <th class="head">Day/Time</th>
            <th class="head">Monday</th>
            <th class="head">Tuesday</th>
            <th class="head">Wednesday</th>
            <th class="head">Thursday</th>
            <th class="head">Friday</th>
        </tr>
        <tr class="row">
            <th class="head">8-10</th>
            <td colspan="3" class="data">Free Slot</td>
            <td class="data">PHY</td>
            <td class="data">CHE</td>
        </tr>
        
        <tr class="row">
            <th class="head">10-12</th>
            <td class="data">GER</td>
            <td class="data">Free Slot</td>
            <td class="data">FWAD</td>
            <td class="data">FWAD</td>
            <td class="data">PHY</td>
        </tr>
        <tr class="row">
            <th class="head">12-1</th>
            <td colspan="5" class="data">LUNCH</td>
        </tr>
        <tr class="row">
            <th class="head">1-3</th>
            <td colspan="2" class="data">Free Slot</td>
            <td class="data">MAT</td>
            <td class="data">MAT</td>
            <td class="data">SS</td>
        </tr>
        <tr class="row">
            <th class="head">3-5</th>
            <td colspan="2" class="data">Free Slot</td>
            <td class="data">Ger</td>
            <td class="data"> CHE</td>
            <td class="data">SS</td>
        </tr>
    </table><br><br>
    <table border="1">
        <tr class="row">
            <th>S.No</th>
            <th>Subject Code </th>
            <th>Subject Name</th>
        </tr>
        <tr>
            <td class="data1">1.</td>
            <td class="data1">19AI414</td>
            <td>Fundamentals of Web Applications Development(FWAD)</td>
        </tr>
        <tr>
            <td class="data1">2.</td>
            <td class="data1">19EN612</td>
            <td>German Basics(GER)</td>
        </tr>
        <tr >
            <td class="data1">3.</td>
            <td class="data1">19PH206</td>
            <td>Physics for Information technology(PHY)</td>
        </tr>
        <tr>
            <td class="data1">4.</td>
            <td class="data1">19CY205</td>
            <td>Principles of Chemistry in Engineering(CHE)</td>
        </tr>
        <tr>
            <td class="data1">5.</td>
            <td class="data1">19MA201</td>
            <td>Calculus and Matrix Algebra(MAT)</td>
        </tr>
        <tr>
            <td class="data1">6.</td>
            <td class="data1">19EY701</td>
            <td>Soft Skills (SS)</td>
        </tr>
    </table>
</body>
</html>
```
### Style.css:
```

.row,.data1
{
    text-align: center;
}
table
{
    width: 600px;
    height:300px
}
.head
{
    background-color: rgb(240, 240, 110);
}
.data{
    background-color: rgb(163, 237, 237);
}
p{
    margin-left: 100px;
}
```

### Views.py:
```
from django.shortcuts import render
def HomePage(request):
    return render(request,'home.html')
```

### Urls.py:
```
from django.contrib import admin
from django.urls import path
from app1 import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.HomePage)
]
```

## OUTPUT
![Screenshot 2024-04-02 161511](https://github.com/Aishwarya-TM/Web-Ex-3/assets/127846109/cf27324e-3f50-4e2f-ba7f-7cec15327b32)


## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
