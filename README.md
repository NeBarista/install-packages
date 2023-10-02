Ansible role: install_nessary_packages
=========



This Ansible role is designed for downloading and installing packages on remote hosts. It can be used to automate the installation of various software packages and libraries on your servers.

Requirements
------------

Before using this role, make sure you have Ansible installed and have SSH access configured to your remote hosts.

Role Variables
--------------

This role uses the following variables, which can be customized in your playbook:

    packages_to_install: A list of packages to be installed. Default value: [].

Dependencies
------------

This role does not have any specific dependencies. However, it relies on Ansible's package management modules to perform package installation tasks.

Example Playbook
----------------

Here's an example playbook that demonstrates how to use this role:

```
---
- name: Install nessary packages on servers
  hosts: all
  become: yes
  roles: 
    - install_nessary_packages
  vars:
    packages_to_install:
      - nmap
      - traceroute
      - vim
      - curl
      - wget

```

License
-------
This Ansible role is licensed under the MIT License. Feel free to modify and distribute it as needed for your projects.
