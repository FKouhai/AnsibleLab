Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.cpus = 4
  end
  config.vm.define "node1" do |node1|
    node1.vm.box = "archlinux/archlinux" 
    node1.vm.network "public_network", ip:"192.168.0.100"
  end
  config.vm.define "node2" do |node2|
    node2.vm.box = "archlinux/archlinux" 
    node2.vm.network "public_network", ip:"192.168.0.101"
  end
  config.vm.define "master" do |master|
    master.vm.box = "hashicorp/bionic64"
    master.vm.network "public_network", ip:"192.168.0.102"
    end
end
