Role Name
=========

create a vm on a KVM (libvirtd) hypervisor with diskfile in a lvm based directory

Requirements
------------

* hypervisor with libvirtd on CentOS7 
* lvm volumegroup must be already created
* a kickstart file on http://software.ii.uib.no/kickstart/$HOSTNAME.ks

Role Variables
--------------

* all settings in defaults/main.yml

Dependencies
------------
* no dependencies

Example Playbook
----------------

''
---
- hosts:
    - "{{ hosts_var }}"
  vars_files:
    - group_vars/all
  become: true

  roles:
    - cr_vm_diskfile
''

License
-------

BSD

Author Information
------------------

olaf.sarnow@uib.no
