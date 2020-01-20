Role Name
=========

Ansible role te define the content of the /etc/resolv.conf file

Requirements
------------

No requrements are needed for this roles

Role Variables
--------------

Define in a group_vars file or in a ./vars/resolv.conf.yml file define the following variables e.g.:
```
resolv_dns_domain: 'cloudalbania.com'
resolv_searchpath: ['cloudalbania.com', 'cloudalbania.local']
resolv_options: 
  - "rotate"
  - "timeout:2"
  - "attempts:2
 
resolv_dns_server:
  - 8.8.8.8
  - 8.8.4.4
```

Variables are defined [here](http://man7.org/linux/man-pages/man5/resolv.conf.5.html).


Dependencies
------------

No dependecies, tested on CentOs 7.

Example Playbook
----------------

This is a sample playbook:

    - hosts: all
      vars_files:
        - ./vars/resolv.conf.yml
      roles:
         - { role: besmirzanaj.ansible_resolv_conf }

License
-------

CC-BY-4.0

Author Information
------------------

This role was created in 2020 by [Besmir Zanaj](https://www.cloudalbania.com/).
