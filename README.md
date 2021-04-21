Documentation: 
1. Development environment version table:
    i) vmware workstation/virtual box version: vmware workstation 
    ii) OS version:
        NAME = "CentOS Linux"
        VERSION = "8"
    iii) Ansible version: ansible 2.10.6
    iv) Python Version
        python version = 3.6.8 (default, Aug 24 2020, 17:57:11) [GCC 8.3.1 20191121 (Red Hat 8.3.1-5)]
    v) Application version (MySQL/RabbitMQ/ElasticSearch/Reddis)
        mysql.x86_64 8.0.21-1

b) Pre-requisites descriptions and it details:
    i) Virtual Machine with CentOS 8
    ii) Enabled EPEl Repositories
    iii) This playbook will take care of all the other Pre-requisites in CentOS. It includes:
         - Python Dependecies
         - Docker Installation
         - Required Repositories
         
c) Detailed manual steps for installing the application. It  should include:
    i) Package that will get installed:
        - python3
        - yum-utils
        - device-mapper-persistent-data
        - lvm2
        - docker-ce
        - docker-ce-cli
        - containerd.io
        - Docker-py
        - MySQL
    ii) Commands to be used
        - chdir
        - yum Commands:
            - yum update
            - add repo
            - yum install
        - pip install
                  
    ii)  The files that will get created or changed
         - MySQL Bind Volume at /opt/var/mysql_data

d) Detailed manual steps for rollback.
    i) package that will be removed. 
        - python3
        - yum-utils
        - device-mapper-persistent-data
        - lvm2
        - docker-ce
        - docker-ce-cli
        - containerd.io
        - Docker-py
        - MySQL

    ii) Commands to be used:
        - 'rm' to remove added repos while rollback
        -  yum Uninstall/autoremove
