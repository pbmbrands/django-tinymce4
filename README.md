django-tinymce
===

**django-tinymce** is a Django application that contains a widget to render a form field as a TinyMCE editor.

**NOTE:** This is a fork of the original django-tinymce here on GitHub. The most basic work has been done to convert it to TinyMCE 4. As such, there are probably bugs.

Quickstart:
===

Install django-tinymce:

    $ pip install git+http://github.com/progressive-cms/django-tinymce4.git#egg=tinymce

Add tinymce to INSTALLED_APPS in settings.py for your project:

    INSTALLED_APPS = (
        ...
        'tinymce',
    )

Add tinymce.urls to urls.py for your project:

    urlpatterns = patterns('',
        ...
        (r'^tinymce/', include('tinymce.urls')),
    )

In your code:

    from django.db import models
    from tinymce.models import HTMLField

    class MyModel(models.Model):
        ...
        content = HTMLField()

**django-tinymce** uses staticfiles so everything should work as expected, different use cases (like using widget instead of HTMLField) and other stuff is available in documentation.

Documentation:
===
http://django-tinymce.readthedocs.org/

** NOTE: These are the docs for the original django-tinymce based on TinyMCE 3.5.8

Support and updates:
===
You can contact me directly at aljosa.mohorovic@gmail.com, track updates at https://twitter.com/maljosa or use github issues.
Be persistent and bug me, I often find myself lost in time so ping me if you're still waiting for me to answer.

License (and related information):
===
Originally written by Joost Cassee.

This program is licensed under the MIT License (see LICENSE.txt)
