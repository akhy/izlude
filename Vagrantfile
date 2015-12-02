# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "server.yml"
  end

  config.vm.provider "virtualbox" do |vb|
     vb.gui = false
     vb.memory = "1024"
  end

  config.vm.define "app" do |app|
    app.vm.box = "debian/jessie64"
    app.vm.hostname = "chickenger.com"
    app.vm.network "private_network", ip: "192.168.100.11"
  end
end
