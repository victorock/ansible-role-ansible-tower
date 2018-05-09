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

The following dependencies are required:

```
---
dependencies:
  - role: geerlingguy.repo-epel
    when: ansible_os_family == 'RedHat'

  - role: geerlingguy.ansible

  - role: victorock.ansible-tower-setup

  - role: geerlingguy.pip
    pip_install_packages:
      - name: ansible-tower-cli
      - name: ansible-tower-cli
        virtualenv: "/var/lib/awx/venv/awx"
      - name: ansible-tower-cli
        virtualenv: "/var/lib/awx/venv/ansible"
      - name: pywinrm
        virtualenv: "/var/lib/awx/venv/awx"
      - name: pywinrm
        virtualenv: "/var/lib/awx/venv/ansible"
      - name: ncclient
        virtualenv: "/var/lib/awx/venv/awx"
      - name: ncclient
        virtualenv: "/var/lib/awx/venv/ansible"
      - name: f5-sdk
        virtualenv: "/var/lib/awx/venv/awx"
      - name: f5-sdk
        virtualenv: "/var/lib/awx/venv/ansible"
      - name: f5-icontrol-rest
        virtualenv: "/var/lib/awx/venv/awx"
      - name: f5-icontrol-rest
        virtualenv: "/var/lib/awx/venv/ansible"
      - name: ipaddress
        virtualenv: "/var/lib/awx/venv/awx"
      - name: ipaddress
        virtualenv: "/var/lib/awx/venv/ansible"
      - name: passlib
        virtualenv: "/var/lib/awx/venv/awx"
      - name: passlib
        virtualenv: "/var/lib/awx/venv/ansible"
      - name: pandevice
        virtualenv: "/var/lib/awx/venv/awx"
      - name: pandevice
        virtualenv: "/var/lib/awx/venv/ansible"
      - name: pan-python
        virtualenv: "/var/lib/awx/venv/awx"
      - name: pan-python
        virtualenv: "/var/lib/awx/venv/ansible"

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
