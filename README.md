Credentials
=========

Create passwords and Kubernetes secrets.

Requirements
------------

Running Kubernetes.

Role Variables
--------------

int_pw_length
dev_pw
manifest_folder
gisnamespace

Dependencies
------------

geogeeksuite.kubernetes

Example Playbook
----------------

---
- hosts: microk8s.test
  vars:
    int_pw_length: 6  
    dev_pw: fooBar
    manifest_folder: 'home/{{ ansible_user }}/manifests'
    gisnamespace: gis
  roles:
  - { role: geogeeksuite.kubernetes,
      tags: kube }
  - { role: geogeeksuite.credentials,
      tags: credentials }


License
-------

Apache License Version 2.0

Author Information
------------------
Created by Marco Bradtke, contact via geogeeksuite.com
