# -*- mode: ruby -*-
# vi: set ft=ruby :

BOX               = "monvillalon/codetrotters" + (['foo'].pack('p').size == 4 ? "32" : "64")
#BOX               = "codetrotters"
NETWORK_INTERFACE = nil
MACHINE_MEMORY    = 512
PRIVATE_IP        = "192.168.2.99"
GUI               = false

Vagrant.configure(2) do |config|

  config.vm.box               = BOX
  config.vm.box_check_update  = true
  config.vm.hostname          = "codetrotters"
  config.vm.network :public_network, bridge: NETWORK_INTERFACE
  config.vm.network :private_network, ip: PRIVATE_IP

  #Setup shared folders
  config.vm.synced_folder "./code", "/home/vagrant/code"

  #Configure Virtual Machine Settings
  config.vm.provider "virtualbox" do |vb|
    vb.gui    = GUI
    vb.memory = MACHINE_MEMORY
  end

end
