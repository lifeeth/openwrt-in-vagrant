# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "openwrt-18.06.0-x86"

  # Change SSH username and pass for vagrant
  config.ssh.username = "root"
  config.ssh.password = "root"
  config.ssh.shell = "/bin/ash"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine.
  # LuCI is accessible from localhost:8080 in this case
  config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network, which allows host-only access to the machine
  # using a specific IP - This is taken over by openwrt as lan.
  config.vm.network "private_network" , ip: "192.168.50.4",
    auto_config: false

  # We do not support vagrant synced folder yet.
  config.vm.synced_folder ".", "/vagrant", disabled: true
end
