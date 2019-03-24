# encoding: utf-8
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "private_network", ip: "10.1.2.1", virtualbox__intnet: "ubuntu-router"
  config.vm.hostname = "ubuntu-router"
  config.vm.synced_folder ".", "/home/vagrant/router"
 # config.vm.provision "shell", inline: <<-SHELL
 #   apt-get update
 # # Install packages 
 #   apt-get install -y netfilter-persistent 
 #   apt-get install -y dnsmasq 
 #   apt-get install -y stubby 
 #   apt-get upgrade -y
 #   apt-get autoremove -y
 # SHELL
  # Set configuration files
#  config.vm.provision "file", source: "stubby.yml", destination: "/etc/stubby/stubby.yml"
#  config.vm.provision "file", source: "dnsmasq.conf", destination: "/etc/dnsmasq.conf"
#  config.vm.provision "shell", inline: <<-SHELL
#    systemctl disable systemd-resolved.service
#    systemctl stop systemd-resolved
#    chown proxy:root /etc/squid/passwd
#  SHELL
end