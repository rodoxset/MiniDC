# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  ## Escolha da Box
  config.vm.box = "ubuntu/bionic64"

  ## DATABASE
  config.vm.define "database" do |db|
    db.vm.network "private_network", ip: "172.17.177.21"
    db.vm.hostname = "database"

    # Configurações de Size da VM
    db.vm.provider "virtualbox" do |v|
      v.name = "database"
      v.memory = 1024
      v.cpus = 2
    end

  end

  ## BLOG
  config.vm.define "blog" do |blog|
    blog.vm.network "private_network", ip: "172.17.177.22"
    blog.vm.hostname = "blog"


    # Configurações de Size da VM
    blog.vm.provider "virtualbox" do |v|
      v.name = "blog"
      v.memory = 1024
      v.cpus = 2
    end

  end
  
    ## BLOG
  config.vm.define 'controller' do |controller|
    controller.vm.network "private_network", ip: "172.17.177.22"
    controller.vm.hostname = "controller"


    # Configurações de Size da VM
    controller.vm.provider "virtualbox" do |v|
      v.name = "MiniDC-AnsibleController"
      v.memory = 1024
      v.cpus = 2
    end

  end

 end