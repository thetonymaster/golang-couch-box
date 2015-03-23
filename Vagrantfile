# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "puppetlabs/ubuntu-12.04-64-nocm"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
  end

  config.vm.define 'localhost' do |machine|
    machine.vm.hostname = 'localhost'
    machine.vm.network "private_network", ip: "192.168.77.22"
  end

end
