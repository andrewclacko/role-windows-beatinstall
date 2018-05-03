Role Name
=========

This role deploys beats to a windows server.  It will remove all previous versions and copy over the metricbeat.yml ttemplates.

Requirements
------------

The windows machine is required to have WINRM enabled so ansible can communicate with the server.
To check connectivity please run ansible -m win_ping IPADDRESS

Role Variables
--------------

The associated playbook variable in group_vars/all has a variable of source
source is the path to where the installer package resided, it is currently set to the elastic download page.

The role has command line variables:

-e "beats=metricbeat/filebeat version=6.0.1 role=servicefabric logstaship=IPADDRESS"

Therefore variables are:

# Desired beat to be installed
beats:
# Desired version of beats
version:
# Server role, e.g. servicefabric
role:
# Ip address of the logstash server
logstaship:


A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
