Vagrant.configure("2") do |config|

  config.vm.define "ubuntu", autostart: true do |subconfig|
   subconfig.vm.box = "ubuntu/bionic64"
   subconfig.vm.provision :shell, path: "createApache.sh"
   subconfig.vm.network "private_network", ip: "10.110.0.10"
   subconfig.vm.hostname = "ubuntu"
   subconfig.vm.network :forwarded_port, guest: 80, host: 8080
  end

  config.vm.define "centos", autostart: true do |subconfig|
   subconfig.vm.box = "centos/7"
   subconfig.vm.network "private_network", ip: "10.110.0.11"
   subconfig.vm.hostname = "centos"
  end

end
