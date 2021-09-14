Role Name
=========

Install the xen orchestra management UI from the github source
will update the repo

Requirements
------------

In Principle, supports any platform that xoa supports. However it's only been
tested on debian-10 buster

Role Variables
--------------

```yaml
vars:
  xoa_admin_user: admin
  xoa_admin_pass: some_complex_pass
```

Dependencies
------------

This role optionally uses the role `limepepper.bootstrap` to install build tools
and git, and some basic utils. You can install these manually and not use bootstrap if required

An installation of nodejs is required, this can be installed using the role
`limepepper.nodejs`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: configure bootstrap
      include_role:
        name: limepepper.bootstrap
      tags: [ bootstrap ]

    - name: configure nodejs
      include_role:
        name: limepepper.nodejs
      vars:
        node_version: 16
      tags: [ nodejs ]

    - name: configure xen-orchestra
      include_role:
        name: limepepper.xen-orchestra
      tags: [ xoa ]

License
-------

BSD

