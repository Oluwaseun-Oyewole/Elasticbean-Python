=====
ebtest
=====

ebtest is a Django app helps in deploying application to ElasticBeanStack with AWS RDS

Quick start
-----------

1. Add "ebtest" to your INSTALLED_APPS setting like this::

    INSTALLED_APPS = [
        ...
        'ebtest',
    ]

2. Include the ebtest URLconf in your project urls.py like this::

    path('ebtest/', include('ebtest.urls')),

3. Run ``python manage.py migrate`` to create the ebtest models.

4. Start the development server and visit http://127.0.0.1:8000/
