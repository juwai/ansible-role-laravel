Ansible Role: Laravel
=========

Prepare folders and files needed for running a Laravel project.

Requirements
------------

Written in Ansible 1.9.*

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

### deploy_user

User owning application code files.

Default is the value of `ansible_ssh_user`.

### deploy_group

Group owning application code files.

Default is the value of `ansible_ssh_user`.

### application_name

Application name used for folders.

### deploy_stage

Stage name used for folders.

### dot_env

Array of key value pairs for application config.

### server_name

Nginx server_name.

### nginx_port

Nginx port.

### laravel_rotate_nginx_log

Use logrotage for the nginx log files.

Default is true.

### laravel_rotate_nginx_log_retention

Retention of the logrotate.

Default is 30.

### laravel_access_control_allow_origin

Enable CORS, and specify Access-Control-Allow-Origin.

Dependencies
------------

juwai.common
juwai.nginx
retr0h.logrotate

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
