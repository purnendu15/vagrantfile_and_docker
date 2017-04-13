# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

#Usage
# vagrant up
# vagrant ssh node1
# vagrant ssh node2
# vagrant ssh node3



Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  (1..3).each do |i|
	config.vm.define "node#{i}" do |web|
		web.vm.box = "ubuntu/trusty64"
	end
	config.vm.hostname = "node#{i}"
	config.vm.network "public_network"
    
	#config.vm.network "public_network", bridge: "wlp1s0"
        #Mention the appropriate bridge interface to override the
        #prompt after vagrant up
  end
end
