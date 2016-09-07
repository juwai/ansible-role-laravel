Ansible Role: Laravel
=========

Prepare folders and files needed for running a Laravel project.

Requirements
------------

Written in Ansible 1.9.*

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

### code_owner

User owning application code files.

Default is the value of `ansible_ssh_user`.

### application_name

Application name used for folders.

### deploy_stage

Stage name used for folders.

### Application config variables

app_env
app_debug
default_app_key
db_host
db_database
db_username
db_password
frontend_lib_url
agentadmin_lib_url
domain_url
cache_driver
session_driver
queue_driver
mail_driver
mail_host
mail_port
mail_username
mail_password
mail_encryption
file_driver
s3_key
s3_secret
s3_region
s3_bucket_name

### Nginx config variables

server_name
port

Dependencies
------------

juwai.common
juwai.nginx

Example Playbook
----------------

    - hosts: servers
        roles:
         - juwai.laravel

License
-------

MIT

Author Information
------------------

This role was created in 2016 by [Juwai Limited](http://www.juwai.com).
