NetBox to BIND DNS Sync
=========

This role provides DNS Synchronization between NetBox and BIND DNS Servers.

Requirements
------------

- Ansible 2.9 or later
- Python 3.x

Role Variables
--------------

Role variables are defined in vars/main.yml, replace below variables as per your environment.
```yaml
---
bind_directory_path: /etc/bind/zones # directory where the zone files are stored
netbox_url: http://192.168.2.9:8000 #URL of the the netbox
netbox_api_token: 40117f4a3ddb6132b87801371f17e8e1398037fd #API Auth token to the NetBox
dns_sync_directory: "/home/labuser/dns-sync" #directory where you will be creating your Virtual Environment and installing the packages
```

Dependencies
------------

All the dependent packages are installed by requirements.txt file.

Example Playbook
----------------

Pleae find below an exmaple playbook on how you can use this role, make sure you define the necessary servers in inventory along with the login credentials:

    - name: NetBox to BIND DNS Sync
      hosts: bind_server
      gather_facts: false
      become: true
      roles:
         - netbox-to-bind-sync

License
-------

BSD

Author Information
------------------

ShoaibMohammed.Shahapuri@wwt.com
