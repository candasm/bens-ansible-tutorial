# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false
  config.vm.define "Web" do |web|
    web.vm.network "private_network", ip: "192.168.33.10"
    web.vm.network "forwarded_port", guest: 80, host: 8080
  end
  config.vm.define "Db" do |db|
    db.vm.network "private_network", ip: "192.168.33.11"
  end
  config.vm.define "App" do |app|
    app.vm.network "private_network", ip: "192.168.33.12"
  end
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1;
  end
end