# Vagrant openwrt

This project helps you to run Openwrt x86 on VirtualBox with Vagrant. 

# Creating a vagrant box

You can utilize the `utils/create_box.sh` to create your own vagrant box with openwrt x86 releases.

# Changes to the image

* The default root password has been set to `root`.
* LuCI and ssh are exposed to the wan interface which is forwarded to your local ports 8080 and 2222 respectively. 
* Fake shutdown script and sudo have been installed to enable `vagrant halt` to work.
* The default WAN has been changed to eth0 and LAN to eth1 to allow vagrant to work.
* Vagrant folder sync does not work with this build.
