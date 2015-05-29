# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network :forwarded_port, host: 4567, guest: 80
  config.vm.synced_folder "salt/roots/", "/srv/salt/"
  config.vm.synced_folder "salt/formulas/", "/srv/formulas/"

  config.vm.provision :salt do |salt|
    salt.verbose = true
    salt.minion_config = "salt/minion.yml"
    salt.run_highstate = true
    salt.colorize = true
    salt.log_level = 'all'
    salt.pillar({
      "owncloud" => {
        "owncloudpass" => "SetAPassword"
       }
    })
  end

  config.vm.provider "virtualbox" do |v|
    v.name = "owncloud_dev"
  end






end
