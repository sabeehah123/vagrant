# -*- mode: ruby -*-
# vi: set ft=ruby :
require "yaml"
vms = YAML.load_file("guest_machines.yaml")
Vagrant.configure("2") do |config|
 vms.each do |machine|
  config.vm.define machine["name"] do |vm|
   vm.vm.box = machine["box"]
   vm.vm.network "private_network", ip: machine["private_ip"]
    machine["scripts"].each do |script|
     vm.vm.provision "shell", path: script
    end 
     vm.vm.provider "virtualbox" do |vb|
       vb.cpus = machine["cpus"]
       vb.memory = machine["memory"]
    end
  end
 end
end
