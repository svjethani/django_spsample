django_spsample
======

Sample django app that uses Stormpath for authentication. It allows users defined in Stormpath to log into the portal. It is based on tutorial by Randall Degges which can be found at http://www.rdegges.com/user-authentication-with-django/

####Pre-reqs
1. Django 
2. Stormpath SDK 
3. Django plugin for stormpath

To install the pre-reqs 

* (optional) 
```virtualenv -p python3 py3env; 
source py3env/bin/activate```
* pip install Django
* Follow steps in the Django plugin for Stormpath readme to install Stormpath SDK and the plugin https://github.com/stormpath/stormpath-django/blob/master/README.md The Stormpath SDK also needed httplib2 and PyYaml. use pip install to install these packages


To use the app follow these steps
* Update settings.py
    + In the DATABASES section, update ENGINE and NAME
    + Replace SECRET_KEY with the appropriate key for your project
    + TEMPLATE_DIRS may need absolute path of the template directory
    + Update STORMPATH_ID, STORMPATH_SECRET, STORMPATH_APPLICATION
* Run the app using django-admin.py django_spsample
* Create accounts in Stormpath in the Application specified in settings.py
* Point your browser at http://localhost:8000 and login using an account created in Stormpath

