# Django-pomidor
https://www.youtube.com/watch?v=FHeAm-JAJ98&list=PLyaCd9XYVI9ACOnDvyto01CH6dx35PG-t&ab_channel=SeniorPomidorDeveloper

-------------------------------------
```
django-admin startproject project
project> manage.py runserver
project>python3 manage.py runserver
project>python3 ./manage.py migrate
project>python3 ./manage.py createsuperuser         -- root
```
--------------------------------------------------
```
project>python3 ./manage.py startapp orders  =add applicitions
project>python3 ./manage.py makemigrations  =create migrrations BD
project>python3 ./manage.py migrate

project>python3 ./manage.py startapp products
project>python3 ./manage.py makemigrations
project>python3 ./manage.py runserver
```
--------------------------------------------------
`project>python3 manage.py shell` -relations many to many
```
in models.py products
    user = models.ForeignKey(User, on_delete=models.CASCADE, null=True)
    products = models.ManyToManyField(Product)
```
```
>>> from orders.models import SalesOrder
>>> order = SalesOrder.objects.all()[1]
>>> order.products.all()`  -- 'NoteBook
```
--------------------------------------------------