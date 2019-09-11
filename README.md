Ansible JBoss EAP Role [![Build Status](https://travis-ci.org/redhat-cop/redhat_sso.svg)](https://travis-ci.org/redhat-cop/redhat_sso)
=================

A role to install Red Hat Single Sign On on RHEL7. Intended to be used with [JBoss Middleware Playbooks](https://github.com/redhat-cop/ansible-middleware-playbooks)

Transfer Method
------------

This role supports a few different mechanism for transferring the product zip files to the target host. These are documented on [the main playbooks README](https://github.com/redhat-cop/ansible-middleware-playbooks), as the methods are supported across a variety of roles.


Dependencies
------------

- [redhat-cop.jboss-common](https://github.com/redhat-cop/ansible-role-jboss-common)
- [redhat-cop.jboss_eap](https://github.com/redhat-cop/jboss_eap)

Our playbooks provide these dependencies in a [common role](https://github.com/redhat-cop/ansible-role-jboss-common), but this there is no explicitly ansible dependency to allow end users more options.

Red Hat SSO Instance Customization
----------------

Red Hat SSO instances can be customized on a per host/group basis by modifying the `jboss_instance` property. By default, a single standalone instance is deployed with HTTP and Management interfaces exposed to all interfaces. 

```
jboss_instances:
  - name: standalone
```

There are several ways in which you can customize the JBoss instances as described below.


* Create a single instance called _standalone_ which does not publicly expose the Management interface

```
jboss_instances:
  - name: standalone
    bind_management_address: 127.0.0.1
```

* Create multiple instances on the same machine with a port offset of 100

```
jboss_instances:
  - name: node1
  - name: node2
    port_offset: 100
```

Example Playbooks
----------------

- [Red Hat SSO 7.2 on RHEL 7](https://github.com/redhat-cop/ansible-middleware-playbooks/blob/master/sso7.2-rhel7.yml)

License
-------

[LICENSE](./LICENSE)

Authors Information
------------------

* [Andrew Block](https://github.com/sabre1041)
