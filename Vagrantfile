# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  if Vagrant.has_plugin? "vagrant-vbguest"
    config.vbguest.no_install  = true
    config.vbguest.auto_update = false
    config.vbguest.no_remote   = true
  end

  config.vm.define :nodo1 do |nodo1|
    nodo1.vm.box = "bento/ubuntu-20.04"
    nodo1.vm.network :private_network, ip: "192.168.100.10"
	nodo1.vm.provision "shell", path: "script.sh"
    nodo1.vm.hostname = "nodo1"
  end

  config.vm.define :nodo2 do |nodo2|
    nodo2.vm.box = "bento/ubuntu-20.04"
    nodo2.vm.network :private_network, ip: "192.168.100.11"
	nodo2.vm.provision "shell", path: "script.sh"
    nodo2.vm.hostname = "nodo2"
  end
end
