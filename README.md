Common
=========

Ansible role to deploy common packages and execute common tasks on a Raspberry Pi

Requirements
------------

A Raspberry pi with SSH enabled

Role Variables
--------------

dns_server: Could be your local PiHole or a public DNS such as8.8.8.8
names_for_lookup_check: ['heise.de','google.com']

Dependencies
------------

-

Example Playbook
----------------

---
- hosts: mypi
  tasks:
  - name: Shut down
    shell:
      cmd: shutdown
    become: true
    tags: ['never','shutdown']
  roles:
  - { role: common,
      tags: ['never','update','setup'] }

License
-------

Appache 2.0

Author Information
------------------

Marco Bradtke