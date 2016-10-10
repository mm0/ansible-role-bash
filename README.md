# README.md

# Ansible Role: Bash v1.0

An Ansible role that configures ~/.bash_aliases for users

Allows you to specify a different list of users with specific bash_aliases for each host group or within a playbook

See Also: ansible-role-sudo, ansible-role-bash, ansible-role-user

![travis-ci](https://travis-ci.org/mm0/ansible-role-bash.svg?branch=master)

## Requirements

Sudo access

## Role Variables

Available variables are listed below, there are no defaults:

		users:
			ubuntu:
				state: present
				groups:  sudo,ubuntu
				sudo: "ALL=(ALL) NOPASSWD: ALL"

Sets PS1 and various aliases defined in vars/main.yml

## Dependencies

None 

## Example Playbook

    - hosts: webservers
      vars:
				users:
					ubuntu:
						state: present
						groups:  sudo,ubuntu
						sudo: "ALL=(ALL) NOPASSWD: ALL"
      roles:
      - ansible-role-bash

## License

MIT

Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

mm0 on github
