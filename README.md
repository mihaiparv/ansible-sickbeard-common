ansible-sickbeard-common
=====

This role installs and configures [SickBeard](http://sickbeard.com/), an awesome
PVR & episode guide that downloads and manages all your TV shows .

Requirements
------------

This role requires Ansible 1.4 or higher and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows.

    # The install directory
    sickbeard_install_dir: '/opt/sickbeard'

    # The user under which the service should run
    sickbeard_user: 'sickbeard'

    # The sickbeard GitHub repository to checkout
    sickbeard_github_repo: 'https://github.com/midgetspy/Sick-Beard.git'

Examples
========

1) Install sickbeard with default settings

    - hosts: all
      roles:
      - ansible-sickbeard-common


2) Install sickbeard with customized install path and runas user.

    - hosts: all
      roles:
      - {role:                  'ansible-sickbeard-common',
         sickbeard_user:        'root',
         sickbeard_install_dir: '/usr/local/sickbeard'}


2) Install sickbeard-tpb (The Pirate Bay edition).

    - hosts: all
      roles:
      - {role:                  'ansible-sickbeard-common',
         sickbeard_github_repo: 'https://github.com/mr-orange/Sick-Beard.git'}

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Parv Mihai

