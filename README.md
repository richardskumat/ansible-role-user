ansible-role-user
=========

My personal ansible role for my managing my users.

This role uses the ansible modules of user and
authorized_keys.

Links to docs:

[user mod](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/user_module.html)

[auth key](https://docs.ansible.com/ansible/latest/collections/ansible/posix/authorized_key_module.html)

Requirements
------------

None

Role Variables
--------------

```
defined_users: []
```

The main task file takes a list of defined users and tries to configure it
on the system.

An example playbook is in molecule/default/converge.yml.


Dependencies
------------

None.

Example Playbook
----------------

There's an example playbook in molecule/default/converge.yml.

License
-------

GPLv3

Author Information
------------------

Richard Skumat

Links
-----

Gitlab

https://gitlab.com/richardskumat/ansible-role-user

Gitlab pipelines

https://gitlab.com/richardskumat/ansible-role-user/pipelines

Github

https://github.com/richardskumat/ansible-role-user
