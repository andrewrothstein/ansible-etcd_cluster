andrewrothstein.etcd-cluster
===========================
[![Build Status](https://travis-ci.org/andrewrothstein/ansible-etcd-cluster.svg?branch=master)](https://travis-ci.org/andrewrothstein/ansible-etcd-cluster)

Configures an etcd cluster. Runs a voting member on every host in the ```etcd-master``` group
and a proxy on the rest of the hosts in the ```etcd``` group.

Requirements
------------

See [meta/main.yml](meta/main.yml)

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

example inventory.ini
```ini
# voting and non-voting members
[etcd]
host[1:n].test

# voting members
[etcd-master]
host[1:3].test
```

in your playbook:
```yml
- hosts: etcd
  roles:
    - andrewrothstein.etcd-cluster
      # if you don't want to secure your install then use
      # etcd_secure: False
```

License
-------

MIT

Author Information
------------------

Andrew Rothstein <andrew.rothstein@gmail.com>
