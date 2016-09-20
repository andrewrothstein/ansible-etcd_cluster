andrewrothstein.etcd-cluster
===========================

Configures an etcd cluster. Runs a voting member on every host in the etcd-master group
and a proxy on the rest of the hosts in the etcd group.

Requirements
------------

See [meta/main.yml]

Role Variables
--------------

See [defaults/main.yml]

Dependencies
------------

See [meta/main.yml]

Example Playbook
----------------

inventory.ini
[etcd]
host[1:n].test

[etcd-master]
host[1:3].test

    - hosts: etcd
      roles:
         - andrewrothstein.etcd-cluster

License
-------

MIT

Author Information
------------------

Andrew Rothstein andrew.rothstein@gmail.com
