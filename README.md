consul-template config update
=========

This role can be used to update a consul-template config, e. g. early in the
startup process before the actual services runs.

[![Build Status](https://travis-ci.org/Rheinwerk/ansible-role-update_consul_template_config.svg?branch=master)](https://travis-ci.org/Rheinwerk/ansible-role-update_consul_template_config)

Notice that it will not start the service and expects the program to be
installed already.

Requirements
------------

The target machine must have consul-template installed.

Role Variables
--------------
There is one main variable that drives this role: `_consul_template`. It is a map that contains all configuration and settings for this role.
Please see `defaults/main.yml` for details.

Dependencies
------------

None.


Example Playbook
----------------

The general contract of this role is to take the variables map `_consul` from `defaults/main.yml` as a template for your configuration and pass that configuration as a parameter to this role.

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        CONSUL_TEMPLATE:
          ...
      roles:
         - { role: update_consul_template_config, tags: [ 'consul_template' ], _consul_template: "{{ CONSUL_TEMPLATE }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Daniel Schneller](https://github.com/dschneller) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.

