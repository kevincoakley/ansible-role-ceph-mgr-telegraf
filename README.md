ansible-role-ceph-mgr-telegraf
==============================

![](https://github.com/kevincoakley/ansible-role-ceph-mgr-telegraf/workflows/Molecule%20Test/badge.svg)

Manage Ceph MGR Telegraf Module - Tested on Ceph Nautilus 

Requirements
------------

Ceph cluster running the Nautilus release, preferably deployed using [ceph-ansible](https://github.com/ceph/ceph-ansible) 

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

None

Example Playbook
----------------

    - name: Converge
      hosts: all
      become: true
    
      vars:
        mgr_telegraf:
          address: udp://172.16.3.12:8094
          interval: 60
    
      roles:
        - role: ansible-role-ceph-mgr-telegraf

License
-------

BSD

Author Information
------------------

Kevin Coakley (https://github.com/kevincoakley)