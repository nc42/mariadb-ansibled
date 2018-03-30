MariaDB
=========
[![Build Status](https://travis-ci.org/nc42/mariadb-ansibled.svg?branch=master)](https://travis-ci.org/nc42/mariadb-ansibled)

A role to install and deploy a MariaDB instance and provision some users.

Requirements
------------

CentOS or Ubuntu.

Role Variables
--------------

- `root_password`: the root password that will be set for the installed instance
- `users`: a list of users to create on the instance. Each user is an object with a `name` and `password` property: `{name: "username", password: "password"}`.

Dependencies
------------

No particular dependency.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { 
              role: mariadb, 
              root_password: "password",
              users: [
                {name: "application", password: "secretpassword"}
              ]
            }

License
-------

MIT