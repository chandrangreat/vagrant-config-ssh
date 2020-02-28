# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.define "control" do |control|
    control.vm.box = "ubuntu/bionic64"
    control.vm.network "private_network", ip: "192.168.33.10"
    control.vm.hostname = "control"
    control.vm.synced_folder ".", "/vagrant", type: "nfs"
    control.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--name", "control"]
      # Customize the amount of memory on the VM:
      vb.memory = "1024"
    end
    control.vm.provision "shell", inline: <<-SHELL
      sudo apt-add-repository ppa:ansible/ansible
      sudo apt-get update
      sudo apt-get install -y ansible
    SHELL
  end
  
  config.vm.define "web01" do |web01|
    web01.vm.box = "ubuntu/bionic64"
    web01.vm.network "private_network", ip: "192.168.33.11"
    web01.vm.hostname = "web01"
    web01.vm.synced_folder ".", "/vagrant", type: "nfs"
    web01.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--name", "web01"]
      # Customize the amount of memory on the VM:
      vb.memory = "1024"
    end
  end
    
end
