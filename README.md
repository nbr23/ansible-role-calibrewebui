ansible-role-calibrewebui
=========

Installs and sets up https://github.com/nbr23/calibre_webui/

Requirements
------------

This role requires the target host to have docker installed.

Role Variables
--------------


Example Playbook
----------------

```
---
- hosts: all
  gather_facts: false
  become: true

  roles:
  - role: ansible-role-calibrewebui
```

License
-------

MIT
