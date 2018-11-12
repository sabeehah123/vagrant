# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "jenkins1" do |jenkins1|
   jenkins1.vm.box = "centos/7"
   jenkins1.vm.network "private_network", ip: "10.0.10.10"
   jenkins1.vm.post_up_message = "Hello, World"
   jenkins1.vm.provider "virtualbox" do |vb|
     #vb.gui = true
     vb.name = "jenkins1"
     vb.cpus = "1"
     vb.memory = "2048"
   end
  end
end
Vagrant.configure("2") do |config|
  config.vm.define "jenkins2" do |jenkins2|
  jenkins2.vm.box = "centos/7"
  jenkins2.vm.network "private_network", ip: "10.0.10.11"
  jenkins2.vm.post_up_message = "Hello, world"
   jenkins2.vm.provider "virtualbox" do |vb| 
    vb.name = "jenkins2"
    vb.cpus = "1"
    vb.memory = "2048"
   end
  end
end
 
