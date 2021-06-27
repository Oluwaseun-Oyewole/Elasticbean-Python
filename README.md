## Creating Django Resuable Package and Deploy to ElasticBeanStack(PAAS) with AWS RDS

## install the following Python 3.6 or later, pip, awsebcli

##### Install awsebcli
    ## pip install awsebcli --upgrade --user

    Add this path to your environmental variables
    ## %USERPROFILE%\AppData\Roaming\Python\Python37\Scripts
    ## %USERPROFILE%\AppData\Roaming\Python\Scripts
    ## eb --versions

##### Creating a django project in a  virtual environment 
    ## python -m venv name-of-project/venv i.e python -m venv ebdjango/venv
    ## cd name-of-project i.e cd ebdjango
    ## venv/Scripts/activate (windows)
    ## venv/Scripts/activate.bat (bash)
    ## pip list or pip freeze (to list all dependencies)
    ## pip install django
    ## django-admin startproject name-ofproject . i.e django-admin startproject ebdjango .(the dot is for the project to be created in the current directory)
    ## pip freeze > requirements.txt
    ## create a .gitignore file
    ## python manage.py startapp name-of-app i.e python manage.py startapp ebtest

  
##### Creating a resuable django app
    ## pip install setuptools --upgrade
    ## create a new folder with django prefix in your parent folder i.e django-name-of-folder(django-ebtest)
    ## copy your application folder() into the new folder
    ## create a README.rst file in your new folder
    ## create a setup.py file in your new folder
    ## create a file named LICENSE.txt  
    ## create a MANIFEST.in file for non file
    ## python setup.py sdist --format=zip for zip folder or python setup.py sdist
    ## python -m pip install  django-ebtest/dist/django-ebtest-3.2.1.zip to install 
    ## python -m pip uninstall django-ebtest to uninstall

##### Setting AWS RDS
    ## https://www.youtube.com/watch?v=Ng_zi11N4_c
    ## run python manage.py migrate


##### Deploying django application to ElasticBeanStack
    ## pip freeze > requirements.txt
    ## mkdir .ebextensions
    ## deactivate (to deactivate your virtual environment)
    ## eb init -p python-3.6 django-tutorial
    ## eb init(select defaults)
    ## eb create django-env
    ## add the domain e.g django-env.eba-whm3fvm6.us-west-2.elasticbeanstalk.com to your allowed hosts in settings.py
    ## eb deploy
    ## eb open


<!-- tw4mNDH0niCEHMFu/CqQHAUqb11D+k4oLojUT4z1 -->