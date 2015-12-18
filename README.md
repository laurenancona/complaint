CCDB-content
============
CCDB-content is a standalone Django project that runs the complaint database app.

## setup

1. copy settings_secret.py.template to settings_secret.py
1. set up virtual environment 

  ```
  mkvirtualenv ccdb
  workon ccdb
  ```
1. install Django 1.6 etc

  ```
  pip install -r requirements.txt
  ```
1. run server

  ``` 
  python manage.py runserver 
  ```
1. install Gulp

  ``` 
  npm install --global gulp
  ``` 
1. install [Autoenv](https://github.com/kennethreitz/autoenv) 

  ```
  $ pip install autoenv
  ```
1. copy `.env_SAMPLE` to `.env` and cd into root directory to execute `.env`.

1. run front end build

  ``` 
  sh ./setup.sh
  ``` 
1. go to landing pages: 
  - http://127.0.0.1:8000/complaintdatabase/
  - http://127.0.0.1:8000/complaintdatabase/data-use/
  - http://127.0.0.1:8000/complaintdatabase/technical-documentation/


***Installing app to your project
Complaint database app can be installed into other Django project by doing the following:

In your Django project `url.py`, you will need to include the following in your `url patterns`:
```python
url(r'^complaintdatabase/', include('complaintdatabase.urls')),
```

In your Django project `settings.py`, you will need to include the following in your `INSTALLED_APPS`:
```python
'complaintdatabase’,
```

Add this to your requirements.txt file:
```
-e git+https://fake.ghe.domain/CCDB4/CCDB-content.git#egg=complaintdatabase
```

Then run the requirements.txt file in your terminal your virtual environment:
```
pip install -r requirements.txt
```

