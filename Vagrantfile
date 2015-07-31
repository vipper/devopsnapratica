# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define :db do |db_config|
    db_config.vm.box = "ubuntu/trusty32"
    db_config.vm.network :private_network, :ip => "192.168.33.10"
    
    db_config.vm.provider 'virtualbox' do |v|
      v.memory = 1024
    end 
  end

  config.vm.define :web do |web_config|
    web_config.vm.box = "hashicorp/precise32"
    web_config.vm.network :private_network, :ip => "192.168.33.12"

    web_config.vm.provider 'virtualbox' do |v|
      v.memory = 2048
    end 
  end

  config.vm.define :monitor do |monitor_config|
    monitor_config.vm.box = "ubuntu/trusty32"
    monitor_config.vm.network :private_network, :ip => "192.168.33.14"

    monitor_config.vm.provider 'virtualbox' do |v|
      v.memory = 1024
    end
  end 

  

end
