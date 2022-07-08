---
Date: 8/7/2022
Author: bugsmaker
Topics: vagrant
---

### Vagrant useful commands

Init vagrant project
> vagrant init <box name or URL\>

Start vagrant to create VM
> vagrant up

Running with provision
> vagrant up --provision

SSH into VM
> vagrant ssh

Shutdown VM
> vagrant halt

Terminate VM and reclaim all resources
> vagrant destroy

Remove the box
> vagrant box list
> vagrant box remove <box-name\>


### Vagrant share
share your VM with another people on Internet

Prerequire: *ngrok* installed for creating network

Install vagrant-share
> vagrant plugin install vagrant-share

Start sharing
> vagrant share

**Note**
When you update your Vagrantfile, you should rerun
> vagrant up --provison

Or destroy previous version of VM first
> vagrant destroy

> vagrant up --provision