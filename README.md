Ansible Tower
=========

Simple Role to Deploy Ansible Tower by Red Hat.

Requirements
------------

None

Role Variables
--------------

None

Dependencies
------------

The following dependencies are defined in `meta/main.yml`:

```
dependencies:
  - role: victorock.ansible-tower-setup
  - role: victorock.ansible-tower-config
```

Example Playbook
----------------

```YAML
- name: "Deploy Ansible Tower by Red Hat"
  hosts: tower
  become: true

  roles:
    - victorock.ansible-tower
```

License
-------

GPLv3

Author Information
------------------

Victor da Costa
