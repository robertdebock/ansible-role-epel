epel
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-epel.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-epel)

Install Extra Packages for Enterprise Linux and CentOS.
Applying this role to other types of operating systems will simply "skip" the job.

Context
--------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/epel.png "Dependency")

Requirements
------------

Access to a repository containing packages, likely on the internet.

Role Variables
--------------

None known.

Dependencies
------------

Include this role to prepare your system.

- [robertdebock.bootstrap](https://travis-ci.org/robertdebock/ansible-role-bootstrap)

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.4|ansible 2.5|ansible 2.6|
|------------|-----------|-----------|-----------|
|centos-6|yes|yes|yes|
|centos-latest|yes|yes|yes|

Example Playbook
----------------

```
---
- hosts: servers
  become: yes

  roles:
    - role: robertdebock.bootstrap
    - role: robertdebock.epel

  tasks:
    - name: install package from EPEL
      package:
        name: ansible-lint
```

Install this role using `galaxy install robertdebock.epel`.

License
-------

Apache License, Version 2.0

Author Information
------------------

[Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
