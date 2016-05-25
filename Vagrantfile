# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define "centos" do |centos|
    centos.vm.box = "centos/7"
    centos.vm.hostname = "centos7.localdomain"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "tests/test.yml"
  end
end
