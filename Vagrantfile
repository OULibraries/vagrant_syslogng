# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "geerlingguy/centos7"
  config.vm.network "private_network", ip: "10.255.255.10"
  config.vm.hostname = "syslogng.vagrant.localdomain"

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
  end
  
  # We use a shell provisioner instead of an Ansible provisioner because of Windows
  config.vm.provision "shell",
    path: "bootstrap.sh", keep_color: "True"
end
