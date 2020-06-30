<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-template-url-optional.svg?maxAge=3600)](https://pypi.org/project/django-template-url-optional/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-template-url-optional.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-template-url-optional.py/actions)

### Installation
```bash
$ [sudo] pip install django-template-url-optional
```

#### Examples
`settings.py`
```python
INSTALLED_APPS = [
    ...
    'django_template_url_optional',
    ...
]
```


```html
{% load url_optional %}

<a href="{% url_optional 'item_list' variable %}">
<a href="{% url_optional 'item_list' %}">
```

`urls.py`
```python
urlpatterns = [
    path('<str:name>/', views.ItemListView.as_view(),name='item_list'),
    path('', views.ItemListView.as_view(),name='item_list'),
]
```

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>