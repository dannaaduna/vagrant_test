# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
    config.vm.define :one do |one_config|
        one_config.vm.box = "precise64"
        one_config.vm.box_url = "http://files.vagrantup.com/precise64.box"
        one_config.vm.network :hostonly, "192.168.2.11"
        one_config.vm.provision :puppet do |puppet|
            puppet.manifests_path = "manifests"
            puppet.manifest_file = "one.pp"
        end
    end

    config.vm.define :two do |two_config|
        two_config.vm.box = "precise64"
        two_config.vm.box_url = "http://files.vagrantup.com/precise64.box"
        two_config.vm.network :hostonly, "192.168.2.12"
        two_config.vm.provision :puppet do |puppet|
            puppet.manifests_path = "manifests"
            puppet.manifest_file = "two.pp"
        end
    end
end