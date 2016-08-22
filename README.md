[![Build Status](https://travis-ci.org/terencewestphal/ansible-role-template.svg?branch=master)](https://travis-ci.org/terencewestphal/ansible-role-template)

Ansible Role: template
=========

A base template for Ansible Roles that builds correctly and can be imported on Ansible Galaxy.

Requirements
------------

- Ansible 2.x

Download
------------
1. Clone this repository into your ansible-playbook environment.  
   
        git clone https://github.com/terencewestphal/ansible-role-template.git roles/__template__

2. Make the appropriate changes to ```meta/main.yml```.
    - Author: NAME
    - Company: COMPANY (optional)
 

Role Variables
--------------

Testing on your local machine

    ansible-playbook roles/__template__/tests/test.yml --extra-vars "rolename=roles/__template__" --syntax-check
    
Testing with Travis CI

    ansible-playbook tests/test.yml -i tests/inventory --extra-vars "rolename=ansible-role-template" --syntax-check

Dependencies
------------

- none

Example Playbook
----------------

    - hosts: localhost
      remote_user: root
      roles:
      - "{{ rolename }}"

License
-------

MIT

Author Information
------------------

- Author: Terence Westphal
- Company: 42 BV