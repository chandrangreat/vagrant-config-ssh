# Vagrant Config for Two Machines

This repository has Vagrant file which can be used to spin up two Virtual Machines having their own private IP addresses. This setup is intended to experiment with ansible as by using one VM as ansible controller and the other VM to be used to execute the tasks specified in playbook.yml.

The vagrant file can be modified for spinning up more than two machine. This setup was just a learning experince of what Vagrant is capable of.

The below [youtube link](https://www.youtube.com/watch?v=GbK7GNwcNrI) is what I used for doing this setup.


There was an issue I faced related to ssh between the machines. I wasn't FOr more info check the below links:

https://superuser.com/questions/671191/how-to-ssh-between-a-cluster-of-vagrant-guest-vms/883065

http://jessesnet.com/development-notes/2014/vagrant-virtual-machine-cluster/