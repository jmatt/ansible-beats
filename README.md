ansible-beats
====================

[![Build Status](https://travis-ci.org/jmatt/ansible-beats.svg?branch=master)](https://travis-ci.org/jmatt/ansible-beats)

Install and configure Elastic [beats](https://www.elastic.co/products/beats) v5 for LSST SQuaRE infrastructure.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: jmatt.beats }

Variables
---------

For complete documentation on configuration options see the [topbeat](https://www.elastic.co/guide/en/beats/topbeat/master/topbeat-getting-started.html), [filebeat](https://www.elastic.co/guide/en/beats/filebeat/master/index.html) and [packetbeat](https://www.elastic.co/guide/en/beats/packetbeat/master/index.html) documentation.

`beats_package_name` *(default "topbeat")* The package name of the beat. Valid options are "topbeat", "filebeat" or "packetbeat".

`beats_install` *(default true)* Whether to install the beat.

`beats_config` *(default "")* The yaml configuration for the beat. If undefined by the user, no configuration will be applied.

`beats_geoip` *(default false)* Wether to install [geoip](https://dev.maxmind.com/geoip/legacy/) for use by the beat.

Acknowledgements
----------------

This role is based on [Jonathan D Strootman's](https://github.com/strootman) Ansible Galaxy role [`cyverse.beats`](https://galaxy.ansible.com/cyverse/beats/). It is a more complete implementation and less opinionated than this role. But it doesn't support v5 or follow the variable naming convention my roles follow. Thus this new role.

I'd highly recommend [`cyverse.beats`](https://galaxy.ansible.com/cyverse/beats/). A big thanks to Strootman and Cyverse for their great roles.

License
-------

The MIT License. See the [LICENSE file](https://github.com/lsst-sqre/ansible-beats/blob/master/LICENSE).