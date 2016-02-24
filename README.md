Role Name
=========

Manage a host entries file as a sane template plus additions

Role Variables
--------------

# defaults file for jamal-fuma.etchosts
etchosts\_hostdb\_path: /etc/hosts-ansible
etchosts\_hostdb\_owner: root
etchosts\_hostdb\_group: admin
etchosts\_hostdb\_mode: 0755
etchosts\_hostdb\_entries:
  - "{{ hostvars[inventory_hostname].ansible_default_ipv4.address }} {{inventory_hostname}}"

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: jamal-fuma.etchosts etchosts_hostdb_path="/etc/hosts" }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
