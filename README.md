ansible-django
==============
[![Build Status](https://travis-ci.org/futurice/ansible-django.svg?branch=master)](https://travis-ci.org/futurice/ansible-django)

Ansible role for [Django](https://www.djangoproject.com/)


Role Variables
--------------
```yaml
---
using_apache: false
using_supervisor: false
using_sqlite: false

app_name: foobar
repo: https://github.com/futurice/django-skeleton.git
git_branch: 'master'
user: www-data
django_settings: "skeleton.settings"

www_root: "/var/www/"
project_path: "{{www_root}}{{app_name}}/"
timestamp: "{{ansible_date_time.epoch}}"
release_path: "{{project_path}}releases/{{timestamp}}/"
release_current: "{{project_path}}current"
virtualenv_path: "{{project_path}}venv/"

apt_packages:
  - git

```


Dependencies
------------
 * futurice.pip


Example Playbook
----------------

    - hosts: servers
      roles:
         - futurice.django

License
-------

BSD
