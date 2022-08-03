# railway
This project shows steps on how to facilitate a production level database with postgres in minutes
Its a huge argument to AWS, facilitation and production time
RAILWAY supports the postgres database structure. The following are steps to connect your project to railway

step 1
Create a new folder
Open your cmd -- windows + r
cd into your new project folder

step 2
Install a virtual environment -- pip install virtualenv
create a virtual env -- virtualenv envname
activate your Virtualenv -- envname\scripts\activate

step 3
Install django -- pip install django

step 4
Install psycopg2 -- pip install psycopg2 
# this is the installation to the connection we need for railway.app 

step 5
Start a Django Project -- django-admin startproject projectname
cd into the project -- cd projectname

step 6
Open your text editor (vscode, pycharm, sublime, etc)
open your project folder
go to the settings.py file 
Locate your database line 
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': '',
    }
 }
 
 
**** Replace it with this ****
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': '',
        'USER': '',
        'PASSWORD': '',
        'HOST': '',
        'PORT': '',
    }
}

step 7
Open your browser and go to railway.app
-create an account
-go to dashboard
-click on new project to create a new project
-open the project
-navigate to variables
-then copy the hashed data individually and replace them in your project settings.py DATABASE
DATABASE_URL *******
PGDATABASE   *******
PGHOST       *******
PGPASSWORD   *******
PGPORT       *******
PGUSER       *******

step 8
go back to your terminal and run -- python manage.py migrate

Thats how you can link your project to the RAILWAY POSTGRES database
