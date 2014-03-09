ansible-couchpotato-common
=====

This role installs and configures [CouchPotato](https://couchpota.to/), an awesome PVR for usenet and torrents.

Requirements
------------

This role requires Ansible 1.4 or higher and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows.

    # The install directory
    couchpotato_install_dir: '/opt/couchpotato'

    # The user under which the service should run
    couchpotato_user: 'couchpotato'

Examples
========

1) Install couchpotato with default settings

    - hosts: all
      roles:
      - ansible-couchpotato-common


2) Install couchpotato with customized install path and runas user.

    - hosts: all
      roles:
      - {role: ansible-couchpotato-common,
         couchpotato_user: 'root',
         couchpotato_install_dir: '/usr/local/couchpotato'}

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Parv Mihai

