ansible-django
==============
[![Build Status](https://travis-ci.org/futurice/ansible-django.svg?branch=master)](https://travis-ci.org/futurice/ansible-django)

Ansible role for [Django](https://www.djangoproject.com/)


Role Variables
--------------
```yaml
---
app_name: foobar
repo: https://github.com/futurice/django-skeleton.git
git_branch: 'master'
user: www-data
django_settings: "skeleton.settings"
```


Dependencies
------------
 * futurice.pip
 * futurice.release


Example Playbook
----------------

    - hosts: servers
      roles:
         - futurice.django

License
-------

BSD
