# vagrant-centos-7
Custom vagrant centos 7 box with Puppet built with Ansible provisioning

## Summary and Instructions

This repo stores build instructions and example on how to create personal vagrant centos box.
Ansible is used for provisioning.

You will need to have VirtualBox and Vagrant installed before proceeding.

## Build instructions

In order to build and deploy the image to your atlas account you will need the Packer tool:
https://www.packer.io/


Once downloaded, just run packer and provide the json file on the root of the repo:
```
~/Downloads/packer build centos7.3.json
```

Additionally, if you want to use the already build CentOS 7.3 version with Puppet 4.10 that comes with this instructions, just:

```
vagrant box add mihailgmihaylov/centos-7.3 --provider virtualbox
```

Or just bring up a new virtualbox instance:

```
vagrant init mihailgmihaylov/centos-7.3; vagrant up --provider virtualbox
```
