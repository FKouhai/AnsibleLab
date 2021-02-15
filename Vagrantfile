Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.cpus = 4
  end
  config.vm.define "node1" do |node1|
    node1.vm.box = "archlinux/archlinux" 
    node1.vm.hostname = "node1"
    node1.vm.network "public_network", ip:"192.168.0.100"
    node1.vm.provider :virtualbox do |vbox|
      vbox.customize ["modifyvm", :id, "--natnet1", "192.168.224.0/24"]
    end
  end
  config.vm.define "node2" do |node2|
    node2.vm.box = "archlinux/archlinux" 
    node2.vm.hostname = "node2"
    node2.vm.network "public_network", ip:"192.168.0.101"
    node2.vm.provider :virtualbox do |vbox2|
      vbox2.customize ["modifyvm", :id, "--natnet1", "192.168.225.0/24"]
    end
  end
  config.vm.define "master" do |master|
    master.vm.box = "archlinux/archlinux"
<<<<<<< HEAD
    master.vm.hostname = "master"
=======
>>>>>>> b097abfe864ecdbcb3c7e9df062d2a009b9a8c48
    master.vm.network "public_network", ip:"192.168.0.102"
    master.vm.provider :virtualbox do |vbox3|
      vbox3.customize ["modifyvm", :id, "--natnet1", "192.168.226.0/24"]
    end
  end
end
