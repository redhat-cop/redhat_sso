Ansible Red Hat Single Sign On (SSO) Role [![Build Status](https://travis-ci.org/redhat-cop/redhat_sso.svg)](https://travis-ci.org/redhat-cop/redhat_sso)
=================

A role to install Red Hat SSO on RHEL7. Intended to be used with [JBoss Middleware Playbooks](https://github.com/redhat-cop/ansible-middleware-playbooks)

Transfer Method
------------

This role supports a few different mechanism for transferring the product zip files to the target host. These are documented on [the main playbooks README](https://github.com/redhat-cop/ansible-middleware-playbooks), as the methods are supported across a variety of roles.


Dependencies
------------

- java
- unzip

Our playbooks provide these dependencies in a [common role](https://github.com/redhat-cop/ansible-middleware-playbooks/tree/master/roles/common), but this there is no explicitly ansible dependency to allow end users more options.

Example Playbooks
----------------

Coming Soon

License
-------

[LICENSE](./LICENSE)

Authors Information
------------------

* [Andrew Block](https://github.com/sabre1041)
