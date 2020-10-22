ansible-role-calibrewebui
=========

Installs and sets up https://github.com/nbr23/calibre_webui/

Requirements
------------

This role requires the target host to have docker installed.

Role Variables
--------------

- `calibre_webui_repo`: Repository to clone calibre_webui from
- `calibre_server_name`: Domain name hosting calibre_webui
- `calibre_tls_cert_dir`: Directory storing the TLS keychain and private key
- `calibre_auth_basic`: Enable basic authentication
- `calibre_auth_basic_file_path`: Path to the basic authentication file
- `calibre_docker_port`: Port to use for the docker container
- `calibre_static_files_path`: Host directory to store and serve the static web files from
- `calibre_static_files_url_path`: url path to the static folder on calibre_server_name
- `calibre_data_dir`: Host directory to mount on the container as calibre library parth
- `calibre_memory_limit`: Memory limitation for the container
- `calibre_user_uid`: UID for the calibre user in the docker container
- `calibre_preferred_format`: output ebook format to default to when converting
- `calibre_local_install_dir`: path to local installation directory


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
