# -*- mode: ruby -*-
# vi: set ft=ruby :
# vim: ts=2 sw=2 et

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

# Vagrant configuration
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # box to use
  config.vm.box = "debian/jessie64"

  # define your hotname here
  config.vm.hostname = "HOSTNAME"

  # define your virtualbox-vm name here
  config.vm.provider "virtualbox" do |v|
    v.name = "VMNAME"
  end

  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.synced_folder "./shared", "/home/vagrant/shared/"

  # set the private ip of the host and configure additional interfaces if needed
  # eth1: hostonly
  config.vm.network "private_network", ip: "192.168.X.X"

  config.vm.provision "shell" do |shell|
    shell.path = "shell/default.sh"
  end

end