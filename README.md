Logstash ansible roles
======================

Setup
-----

Generate SSL keys by running:

    openssl req -x509 -batch -nodes -newkey rsa:2048 -keyout logstash-forwarder.key -out logstash-forwarder.crt

Copy the resultant .key and .crt files to `roles/logstash/files/certs`.

Copy `vars/global_vars.yml.sample` and customise it to suit your setup - it should be fairly self explanatory.

Add the `logstash` groups to your ansible hosts file

Installation
------------

### Logstash:

`ansible-playbook logstash.yml`
