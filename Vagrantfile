# -*- mode: ruby -*-
# vi: set ft=ruby :

NETWORK_INTERFACE = nil
MACHINE_MEMORY    = 512
PRIVATE_IP        = "192.168.99.99"

Vagrant.configure(2) do |config|

  config.vm.box               = "monvillalon/codetrotters"
  config.vm.box_check_update  = true
  config.vm.hostname          = "codetrotters"
  config.vm.network :public_network, bridge: NETWORK_INTERFACE
  config.vm.network :private_network, ip: PRIVATE_IP

  #Setup shared folders
  config.vm.synced_folder "./code", "/home/vagrant/code"

  #Configure Virtual Machine Settings
  config.vm.provider "virtualbox" do |vb|
    vb.gui    = false
    vb.memory = MACHINE_MEMORY
  end

end
