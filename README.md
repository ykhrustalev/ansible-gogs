Role Name
=========

Installs GOGS http://gogs.io/ to debian based box with postgres

Requirements
------------

No initial requirements

Role Variables
--------------

Postgresql
    
    gogs_db_name: gogs
    gogs_db_user: gogs
    gogs_db_password: jh3wk92km1e09
    gogs_db_host: 127.0.0.1
    gogs_db_port: 5432
    
OS user

    gogs_app_user: git
    gogs_app_group: git
   
Where to install gogs
   
    gogs_app_home: /home/git/gogs
    
Where to keep git repositories

    gogs_repos_home: /home/git/gogs-repositories
    
Logs folder

    gogs_log_root: /var/log/gogs
    
Gogs service hostname

    gogs_app_hostname: gogs.example.com

Gogs service email user

    gogs_app_email: gogs@example.com

Gogs service bind address and url

    gogs_app_url: http://{{gogs_app_hostname}}/
    gogs_app_bind_address: localhost
    gogs_app_bind_port: 3000
    
Where to get gogs binaries

    gogs_dist_version: v0.6.1
    gogs_dist_url: https://github.com/gogits/gogs/releases/download/{{gogs_dist_version}}/linux_amd64.zip
    gogs_dist_sha256: ab4d8341d1c14e753914b68b3ec0c9b169c361123dcef541ff34444b1e54812b
    gogs_tmp_folder: ~/


Dependencies
------------

No at the moment

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: ykhrustalev.gogs}

License
-------

MIT

Author Information
------------------

GOGS authors for gogs and init, app configs.

Yuri Khrustalev for the ansible role
