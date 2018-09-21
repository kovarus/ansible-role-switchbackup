switchbackup
=========

This role is used to backup configurations of various switch platforms.

Requirements
------------

The following python libraries are required for backing up Juniper devices:
 - ncclient
 - junos-eznc
 - jxmlease

Role Variables
--------------

The following variables are available with defaults set in `defaults/main.yml`:

    backup_dir
The root directory to store the configuration files.

    backup_full_path
The full path (including filename ) for the configuration files. This must be unique for each host.

This role assumes that the following variables are set
  - ansible_network_os
  - ansible_become
  - ansible_become_method
  - ansible_connection
  - ansible_user
  - ansible_password
  - ansible_become_pass

Dependencies
------------

This role depends on the following roles:
 - juniper.junos

Example Playbook
----------------
    ---
    - hosts: switches
      gather_facts: no
      roles:
        - kovarus.switchbackup

Platforms Supported
-------------------
  - Cisco IOS
  - Cisco NX-OS
  - Juniper JUNOS

License
-------

Apache License 2.0
