icinga
======

Installs and configures Icinga

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name           | Default | Description                  |
|----------------|---------|------------------------------|
| icinga_version | 2.4.1   | Version of Icinga to install |

Dependencies
------------

None

Example Playbook
----------------

Install Icinga
```
- hosts: all
  roles:
    - kbrebanov.icinga
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
