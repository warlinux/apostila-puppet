# -*- mode: ruby -*-

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  config.vm.define "apostila" do |apostila|
    apostila.vm.hostname = "apostila.instruct"
    apostila.vm.box = "puppetlabs/debian-6.0.10-64-puppet"
    apostila.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--ioapic", "on"]
      v.cpus = 2
      v.memory = 1024
    end
    config.vm.provision "puppet" do |puppet|
      puppet.environment_path = "environments"
      puppet.environment = "production"
    end
  end

end
