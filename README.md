[![Build Status](https://travis-ci.org/terencewestphal/ansible-role-template.svg?branch=master)](https://travis-ci.org/terencewestphal/ansible-role-template)

Ansible Role: template
======================

A base template for Ansible Roles that builds correctly and can be imported on Ansible Galaxy.

Requirements
------------

- Python 2.7
- Ansible 2.x

Installation
------------

Installing roles from Ansible Galaxy:

    $ ansible-galaxy install username.rolename
    
You can specify a directory where you want the downloaded roles to be placed, 
this is very useful when you use this template as a starting point for creating new roles.
 
    $ ansible-galaxy install username.rolename -p ~/ansible/roles/__template__

Role Variables
--------------

Testing on your local machine

    $ ansible-playbook roles/__template__/tests/test.yml --extra-vars "rolename=roles/__template__" --syntax-check
    
Testing with Travis CI

    $ ansible-playbook tests/test.yml -i tests/inventory --extra-vars "rolename=ansible-role-template" --syntax-check

Dependencies
------------

Install all dependencies needed for this role.

    $ cd ~/path/to/ansible/role
    $ ansible-galaxy install -r requirements.yml

Required dependencies: 
- none

Example Playbook
----------------
***(content taken from test.yml)***

    - hosts: localhost
      remote_user: root
      roles:
      - "{{ rolename }}"

Role Development
------------
The primary use case for this codebase is Role Development.

1. Clone this repository into your ansible-playbook environment.  

        $ git clone https://github.com/terencewestphal/ansible-role-template.git roles/__template__

2. Make the appropriate changes to ```meta/main.yml```.
    - [ ] author
    - [ ] company
    - [ ] platforms
    - [ ] galaxy_tags
    - [ ] dependencies

3. Add Files, Tasks, Vars, Templates etc to the role.
    - [ ] defaults
    - [ ] files
    - [ ] handlers
    - [ ] modules
    - [ ] plugins
    - [ ] tasks
    - [ ] templates
    - [ ] tests
    - [ ] vars
    
4. Update the ```README.md``` to reflect the changes you made.
    
5. Publish your new role.
    - [ ] Push to Github
    - [ ] Test with Travis CI
    - [ ] Publish in Ansible Galaxy
    
License
-------

MIT

Author Information
------------------

- Author: Terence Westphal
- Company: 42 BV
