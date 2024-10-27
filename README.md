Ansible Role: Plex-QNAP
=======================

Install or update Plex Media Server on QNAP NAS.

- https://www.plex.tv/
- https://www.plex.tv/media-server-downloads/?cat=nas&plat=qnap

Requirements
------------

A QNAP NAS.

Role Variables
--------------

Available role variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
# Download directory for qpkg package
plex_download_dir: /tmp

# Your Plex server URL (for version check)
plex_server_url: https://plex.example.net

# Optional token (For beta server update channel, requires Plex Pass)
# https://support.plex.tv/articles/204059436-finding-an-authentication-token-x-plex-token/
plex_token:
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: all

  gather_facts: true
  gather_subset:
    - "!all"
    - "!min"
    - architecture

  roles:
    - djuuu.plex_qnap
```

License
-------

Beerware License
