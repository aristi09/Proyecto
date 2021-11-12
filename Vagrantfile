# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
if Vagrant.has_plugin? "vagrant-vbguest"
  config.vbguest.no_install = true
  config.vbguest.auto_update = false
  config.vbguest.no_remote = true
end
config.vm.define :nginx do |nginx|
nginx.vm.box = "bento/centos-7.9"
nginx.vm.network :private_network, ip: "192.168.100.2"
nginx.vm.hostname = "nginx"
end
config.vm.define :backend1 do |backend1|
backend1.vm.box = "bento/centos-7.9"
backend1.vm.network :private_network, ip: "192.168.100.3"
backend1.vm.hostname = "backend1"
end
config.vm.define :backend2 do |backend2|
backend2.vm.box = "bento/centos-7.9"
backend2.vm.network :private_network, ip: "192.168.50.4"
backend2.vm.hostname = "backend2"
end
end