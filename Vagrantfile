# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.require_version ">= 1.8.0"

Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2304"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "main.yml"
  end
end
