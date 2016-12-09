Ansible Role: Bash v1.0
=====================

[![Build Status](https://travis-ci.org/mm0/ansible-role-bash.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-bash)


An Ansible role that configures ~/.bash_aliases for users

Allows you to specify a different list of users with specific bash_aliases for each host group or within a playbook

See Also: ansible-role-sudo, ansible-role-bash, ansible-role-user


Requirements
---------------

- Sudo access

Role Variables
---------------

Available variables are listed below, there are no defaults:

```yml
users:
    ubuntu:
        state: present
        groups:  sudo,ubuntu
        sudo: "ALL=(ALL) NOPASSWD: ALL"
```

Sets PS1 and various aliases defined in vars/main.yml

Dependencies
---------------

None 

Example Playbook
---------------

```yml
- hosts: webservers
  vars:
    users:
        ubuntu:
            state: present
            groups:  sudo,ubuntu
            sudo: "ALL=(ALL) NOPASSWD: ALL"
  roles:
  - ansible-role-bash
```

License
---------------

BSD-2

Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

[mm0](https://github.com/mm0) on github
