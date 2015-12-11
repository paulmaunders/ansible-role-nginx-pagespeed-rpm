nginx-pagespeed
=========

This role can be used to create an RPM for nginx with support for Google's pagespeed module. It works by re-building the original nginx source RPM with the additional Pagespeed module included.

Requirements
------------

This has currently been tested against a [Centos 7 box](https://github.com/paulmaunders/vagrant-nginx-pagespeed-rpm), but I hope to add debian and other distro support in the future.

Role Variables
--------------

* nps_version: 1.9.32.10 - the nginx pagespeed version
* nginx_version: 1.8.0 - the nginx version
* build_dir: /tmp/build-nginx-pagespeed - the build directory (leave this)
* nps_release: release-{{nps_version}}-beta - the nginx page speed release file pattern (leave this unless Google change their naming conventions) 

Dependencies
------------

N/A

Example Playbook
----------------

Here's an example of how to use with a vagrant box...

```
- hosts: default
  user: vagrant
  sudo: True
  gather_facts: True
  roles:
    - ansible-role-nginx-pagespeed-rpm
```

License
-------

BSD

Author Information
------------------

Paul Maunders (https://github.com/paulmaunders)
