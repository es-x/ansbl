# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  #using ident key for all machines
  config.ssh.insert_key=false

  config.vm.define "c7study1" do |c7study1|
  c7study1.vm.box = "centos/7"
  c7study1.vm.box_check_update = "true"
  #c7study1.vm.network "forwarded_port", guest: 80, host: 8080
  #c7study1.vm.network "forwarded_port", guest: 443, host: 8443
  c7study1.vm.network "private_network", ip: "172.16.99.15"
  c7study1.vm.provider "virtualbox" do |v|
    v.name = "c7study1"
  end
  end
  config.vm.define "c7study2" do |c7study2|
  c7study2.vm.box = "centos/7"
  c7study2.vm.box_check_update = "true"
  c7study2.vm.network "forwarded_port", guest: 80, host: 8081
  c7study2.vm.network "forwarded_port", guest: 443, host: 8444
  c7study2.vm.provider "virtualbox" do |v|
    v.name = "c7study2"
  end
  end
  config.vm.define "c7study3" do |c7study3|
  c7study3.vm.box = "centos/7"
  c7study3.vm.box_check_update = "true"
  c7study3.vm.network "forwarded_port", guest: 80, host: 8082
  c7study3.vm.network "forwarded_port", guest: 443, host: 8445
  c7study3.vm.provider "virtualbox" do |v|
    v.name = "c7study3"
  end
  end
end
