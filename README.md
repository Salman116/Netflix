# Netflix
Netflix clone

Set up a virtual environment
Install Django
Set up a Django project
Start a Django app

1. Make a new folder 

2- Make Virtual environment
	py -3.8 -m venv venv  ( to use multiple python verions)
	python -m venv venv

3- Activate Virtual environment

4- Install Django
	pip install django

5- django-admin startproject netflix

6- python manage.py startapp app

7- Add your app in installed apps in settings of project

8- import os in setting file
	os.path.join(BASE_DIR, 'templates')

9- Make 2 folders
	static
	templates

10- Make STATIC_URL, STATIC_ROOT, MEDIA_ROOT, MEDIA_URL

11- write static and media urls in project urls
from django.conf.urls.static import static
from django.conf import settings
	if settings.DEBUG:
    		urlpatterns += static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)	
		urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)

12- Add app urls to project urls:
	path('', include('app.urls'))

13- Now make urls file and utils file:
	make a urls and respective view
