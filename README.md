Ansible Naemon playbook
=====

This role installs and configures Naemon on a server.
You can also specify if it needs to install Thruk as well and set the default
admin password.
This playbook is only compatible for Debian.

Requirements
------------

This role requires Ansible 1.4 or higher and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows:

```
    # Set it to True if you want to install Thruk
    install_thruk: True
    # Set the Thruk Admin user password
    thruk_admin_password: <password>
```

Examples
========

```
# Roles
- name: deploy Naemon
  hosts: monitoring
  user: root

  roles:
    - naemon

  vars:
    - install_thruk: True
    - thruk_admin_password: admin
```

Dependencies
------------

None

License
-------

GPL

Author Information
------------------

Pierre Mavro / deimosfr


