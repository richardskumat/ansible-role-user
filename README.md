ansible-role-user
=========

A very primite role that adds a single user with sudo rights, and then
adds a local ~/.ssh/id_rsa.pub to remote user's authorized_keys.

Requirements
------------

None

Role Variables
--------------

```
# what username to use
username: "qwe"
# this is the first default uid used by default debian installations
# most likely will be assigned to a default sudo/admin user on cloud images
# eg admin on aws, or debian user on ovh
# or whatever user someone adds as a first user in a manual/preseed install
# this is unused at this time
uid: "1000"
shell: "/bin/bash"
# hunter2
password_var: "$6$JE/i1W/m6t3$y2GRMvAUseTxaqN1aSXKEfShb84oCblPGqYYhvrPyEvoD6EVZOfLrFQ.CkYrS8YlygXRA9pivlyB8PkSs6h9u1"
# https://stackoverflow.com/questions/54373152/how-to-resolve-could-not-locate-file-in-lookup-reading-id-rsa-pub
ssh_key_path: "{{ lookup('file', lookup('env','HOME') + '/.ssh/id_rsa.pub') }}"
# whether to create or remove this user
# present or absent
user_state: present
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: user, x: 42 }

License
-------

GPLv3

Author Information
------------------

Richard Skumat

https://github.com/richardskumat
