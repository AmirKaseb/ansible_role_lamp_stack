  Lamp\_Stack\_Initiliaze

Lamp\_Stack\_Initiliaze
=======================

A role to initialize and configure a LAMP stack (Linux, Apache, MySQL, PHP) on Ubuntu servers.

Requirements
------------

*   Ubuntu 18.04 (Bionic) or 20.04 (Focal)
*   Ansible 2.9 or higher

Role Variables
--------------

The following variables can be set to customize the role:

*   `apache_port`: Port for the Apache server (default: 80)
*   `mysql_root_password`: Root password for MySQL (default: 'rootpassword')
*   `php_version`: PHP version to install (default: '7.4')

Example of default variables in `defaults/main.yml`:

    apache_port: 80
    mysql_root_password: 'rootpassword'
    php_version: '7.4'

Dependencies
------------

No external role dependencies.

Example Playbook
----------------

    - hosts: servers
      become: yes
      roles:
        - role: AmirKaseb.Lamp_Stack_Initiliaze
          vars:
            apache_port: 8080
            mysql_root_password: 'securepassword'
            php_version: '8.0'

License
-------

BSD

Author Information
------------------

This role was created in 2024 by Amir Kaseb. For more information, visit [your website](https://example.com) or contact via [email@example.com](mailto:email@example.com).
