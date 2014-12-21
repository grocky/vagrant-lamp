# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  
  config.vm.network :private_network, ip: "192.168.10.10"

  # Forward ports to Apache and MySQL
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 3306, host: 33060
  
  config.vm.synced_folder "www", "/var/www/html", create: true
  config.vm.provision "shell", path: "provision.sh"
  
  config.vm.provider "virtualbox" do |vb|
    vb.name = 'grocky-vagrant-lamp'
    vb.memory = 512
    vb.cpus = 2
  end
end
