Sudo
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.sudo-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/sudo)
[![Build Status](https://travis-ci.com/samdoran/ansible-role-sudo.svg?branch=master)](https://travis-ci.com/samdoran/ansible-role-sudo)

Setup basic `sudo` configuration to passwordless `sudo` for use with Ansible. This is mainly needed on new hosts to get them in a state to be mananged by Ansible.

Requirements
------------

None.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `` | `` |  |


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

    - hosts: all
      roles:
         - samdoran.sudo

License
-------

Apache 2.0
