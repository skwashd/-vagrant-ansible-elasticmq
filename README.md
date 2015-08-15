# Vagrant Ansible ElasticMQ

This is generally useful when you need to Amazon SQS in local/offline
development environments.

A vagrant machine for [ElasticMQ](https://github.com/adamw/elasticmq). The
provisioning is handled by Ansible. The base box is 32 bit Ubuntu 14.04 using 
VirtualBox.

## Install

Ensure you have vagrant, ansible and virtualbox all installed and working on
your machine.  Then follow these steps:

* Clone this repo
* Install the dependencies from ansible galaxy
  `sudo ansible-galaxy install aisch.elasticmq ansiblebit.oracle-java`
* `vagrant up` and away you go

