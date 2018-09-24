[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

icinga
======

Installs and configures Icinga

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                     | Default    | Description                                 |
|--------------------------|------------|---------------------------------------------|
| icinga_version           | 2.4.1      | Version of Icinga to install                |
| icinga_web_enable        | false      | Whether to install the web interface or not |
| icinga_database_server   | postgresql | Database server to use for web interface    |
| icinga_database_password | icinga     | Database password                           |
| icinga_web_server        | nginx      | Web server to use for web interface         |

Dependencies
------------

- kbrebanov.postgresql (When web is enabled and database server is postgresql)
- kbrebanov.nginx (When web is enabled and web server is nginx)

Example Playbook
----------------

Install Icinga
```
- hosts: all
  roles:
    - kbrebanov.icinga
```

Install Incinga, enable web interface and use PostgreSQL/nginx
```
- hosts: all
  vars:
    icinga_web_enable: true
    icinga_database_server: postgresql
    icinga_web_server: nginx
  roles:
    - kbrebanov.icinga
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
