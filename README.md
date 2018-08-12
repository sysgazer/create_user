create_user
=========

Create a user and upload an ssh public for remote authentication

Requirements
------------

No specific requried Ansible
Needs a default ssh public key or a specific key needs to be called out in a variable.

Role Variables
--------------

#Define the user you would like to create
user_name: default

#Define the user state present or absent
user_state: present
#Define the path to the ssh public key
ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------

None

Example Playbook
----------------
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: sysgazer
         ssh_key: ~/.ssh/id_rsa_ansible.pub



License
-------

MIT

Author Information
------------------

info@kumul.us
