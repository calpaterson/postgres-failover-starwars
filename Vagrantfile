# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  if Vagrant.has_plugin?('vagrant-cachier')
    config.cache.auto_detect = true
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision.yml"
  end

  config.vm.define :luke do |luke|
    luke.vm.box = "ubuntu/trusty64"
    luke.vm.network :private_network, ip: "10.0.0.2"
  end

  config.vm.define :han do |han|
    han.vm.box = "ubuntu/trusty64"
    han.vm.network :private_network, ip: "10.0.0.3"
  end

  config.vm.define :leia do |leia|
    leia.vm.box = "ubuntu/trusty64"
    leia.vm.network :private_network, ip: "10.0.0.4"
  end
end
