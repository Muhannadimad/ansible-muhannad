# Ansible Task #
## requirements ##
- CentOs 7
- epel-release pkgs
- Ansible

## structure ##
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
├── pexpect
│   ├── info_idpl_55435118_distro_opensuse_com_python3-pexpect3-3.1-4.1.x86_64.rpm
│   ├── info_idpl_55435118_distro_opensuse_com_python3-pexpect3-3.1-4.1.x86_64.rpm.html
│   └── python-pexpect-4.8.0-1-omv4050.noarch.rpm
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
