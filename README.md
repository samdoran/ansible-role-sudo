sudo
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.sudo-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/sudo)

Setup basic `sudo` configuration to allow passwordless `sudo` and not require a TTY. This is mainly needed on new hosts to get them in a state to be managed by Ansible.

Requirements
------------

None.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `sudo_package_name` | `sudo` | Name of `sudo` package to install.  |
| `sudo_owner` | `root` | User that owns the `sudoers` files. |
| `sudo_group` | `group` | Group that owns the `sudoers` files. |
| `sudo_default_options` | `ALL=(ALL) NOPASSWD: ALL` | Default options applied to `sudo_owners` and `sudo_groups` if per user or group options are not specified.|
| `sudo_sudoers_path` | `/etc/sudoers` | Path to `sudoers` file.  |
| `sudo_sudoers_d_path` | `/etc/sudoers.d` | Path to `sudoers.d` directory. |
| `sudo_sudoers_lines` | `[see defaults/main.yml]` | Lines to insert in `/etc/sudoers`. By default, the lines inserted disable the requirement for a TTY and ensure the `sudo_sudoers_d_path` is read. |
| `sudo_users` | `[]` | List of users and their `sudo` options. If no `options` are specifid, `sudo_default_options` will be used. See `defaults/main.yml` for examples. |
| `sudo_groups` | `[]` | List of groups and their `sudo` options. If no `options` are specifid, `sudo_default_options` will be used. If the group does not exist, it will be created. See ` defaults/main.yml` for examples. |
| `sudo_create_groups` | `yes` | Whether or not to create `sudo_groups`. |


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      roles:
         - samdoran.sudo

License
-------

Apache 2.0
