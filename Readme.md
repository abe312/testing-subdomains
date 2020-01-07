This project is made to test out [subdomains](https://github.com/abe312/django-subdomains) library

```
/etc/hosts

127.0.0.1 api.example.com
127.0.0.1 www.example.com
127.0.0.1 example.com
```

#### example.com:8000 displays hello world!

#### api.example.com:8000 displays API

#### www.example.com:8000 displays FRONTEND

> tested on django1.11.27, django2.2.9 and django3.0.2

##### for using a different url domain name other than 'example.com':

./manage.py shell

```
>>> from django.contrib.sites.models import Site
>>> one = Site.objects.all()[0]
>>> one.domain = 'myveryspecialdomain.com'
>>> one.name = 'My Special Site Name'
>>> one.save()
```

##### Then set SITE_ID in settings.py accordingly

credit: [stackoverflow](https://stackoverflow.com/questions/12289148/where-do-i-set-the-domain-for-my-django-sites-framework-site-when-i-only-have-o/12289245#12289245)
