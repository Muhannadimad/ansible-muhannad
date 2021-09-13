# Ansible Task #
## requirements ##
- CentOs 7
- epel-release pkgs
- Ansible

## structure ##
```
.
├── ansible.cfg
├── conf_zabbix.yml
├── create_db.yml
├── gather_facts.yml
├── host_vars
│   ├── 172.20.51.181.yml
│   ├── 172.20.51.182.yml
│   └── 172.20.51.183.yml
├── httpd.yml
├── install_mariadb.yml
├── install_php.yml
├── install_pkgs.yml
├── install_requirements.yml
├── install_zabbix.yml
├── inventory
├── README.md
├── roles
│   ├── apache
│   │   ├── handlers
│   │   │   └── main.yml
│   │   └── tasks
│   │       └── main.yml
│   ├── common
│   │   ├── handlers
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── templates
│   ├── conf_zabbix
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── templates
│   │   │   └── zabbix_server.conf.j2
│   │   └── vars
│   │       └── main.yml
│   ├── create_db
│   │   └── tasks
│   │       └── main.yml
│   ├── install_mariadb
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── vars
│   │       └── main.yml
│   ├── install_php
│   │   └── tasks
│   │       └── main.yml
│   ├── install_pkgs_client
│   │   └── tasks
│   │       └── main.yml
│   ├── install_pkgs_server
│   │   └── tasks
│   │       └── main.yml
│   ├── install_requirements
│   │   └── tasks
│   │       └── main.yml
│   ├── install_zabbix
│   │   └── tasks
│   │       └── main.yml
│   ├── local
│   │   └── tasks
│   │       ├── main-backup.yml
│   │       └── main.yml
│   └── selinux
│       └── tasks
│           └── main.yml
├── selinux.yml
└── site.yml
```
## roles ##
- apache: configure apache in local
- local: move .rpms to www directory and create repo
- common: add yum repo (my_zabbix) to all machine and clean cash
- selinux: make mode permissive
- install_requirements: install epel-release , disable php repo
- install_php: install php pkgs and config time in php.ini
- install_mariadb: install and configure mariadb
- create_db: create database for zabbix
- install_zabbix: install zabbix pkgs in local (['zabbix-server-mysql','zabbix-web-mysql','zabbix-agent','zabbix-get'])
- install_pkgs_client: install zabbix client pkgs on the client
- install_pkgs_server: install zabbix server pkgs on the server
- conf_zabbix:
              1- Edit the Zabbix Apache configuration file.
              2- Import the MySQL dump file (this file installed with zabbix pkg)
              3- Modify the Zabbix configuration file with Database details.
              4- Modify firewall rules:
                      * add http, https services
                      * add 10051, 10050 ports
