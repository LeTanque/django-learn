# django-learn

> example `.gitignore`

> Installs the django framework:   `python -m pip install Django`

> Generate the template:   `django-admin startproject  myprojectname`

> Tastypie is a REST framework:   `pip install django-tastypie`

> From inside of mysite:   `python manage.py startapp api`

Once the models have been set, run the migrations like this:

> `python manage.py makemigrations`

> `python manage.py migrate`

You will get some messages about the migrations and the sqlite3 db will be created at the top level.

Check to make sure it works by dropping into a shell and manually adding a note.

> Drop into shell:   `python manage.py shell`


> Start the api using:   `python manage.py runserver`





```
>>> from api.models import Note
>>> note = Note(title="First Note", body="This is certainly noteworthy")
>>> note.save()
>>> Note.objects.all()
<QuerySet [<Note: First Note This is certainly noteworthy>]>
>>> exit()
```

We create our note, save it, then retrieve all notes. You can see our `__str__` method at work, returning both the title and the body.


##### Notes
Folder structure:
```
mysite
-- api
-- -- migrations
-- -- -- __init__.py
-- -- __init__.py
-- -- admin.py
-- -- apps.py
-- -- >> etc
-- mysite
-- -- __init__.py
-- -- settings.py
-- -- urls.py
-- -- >> etc
-- manage.py
```


The mysite folder inside of mysite contains the settings for the 
configuration of the project, as well as exposing URLs. 

The api folder handles API magic, which I suppose means routing to db.
