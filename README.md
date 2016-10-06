devstack
========

[![Build Status](https://travis-ci.org/dstanek/ansible-role-devstack.svg?branch=master)](https://travis-ci.org/dstanek/ansible-role-devstack)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dstanek.devstack-blue.svg)](https://galaxy.ansible.com/dstanek/devstack/)

A role to install and run devstack.

Requirements
------------

None

Role Variables
--------------

Devstack specific settings.

    devstack_repo: "git://github.com/openstack-dev/devstack.git"
    devstack_keep_running: true
    devstack_reclone: "no"

    # customize what services are enabled in devstack
    devstack_enabled_services: key,mysql


Keystone specific settings.

    devstack_identity_backend: "sql"
    devstack_token_type: "fernet"
    devstack_install_tempest: True
    devstack_keystone_identity_backend: "sql"
    devstack_password: "password"
    devstack_service_token: "password$$"

    # only used if devstack_keystone_identity_backend is 'ldap'
    devstack_keystone_clear_ldap: "yes"
    devstack_ldap_password: "password"

Dependencies
------------

None

Example Playbook
----------------

Install and run devstack

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
        - dstanek.devstack

License
-------

Apache 2.0

Author Information
------------------

David Stanek <dstanek@dstanek.com>

http://traceback.org
