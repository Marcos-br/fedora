Vagrant.configure("2") do |config|

  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"
  
  config.vm.box = "generic/fedora38"

  config.vm.hostname = "fedora38-vm"

  config.vm.network "public_network", type: "dhcp"

  config.vm.synced_folder "code/", "/home/vagrant/code"
 
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.name = "fedora38"
    vb.memory = "4096"
    vb.cpus = "4"
  end

  config.vm.provision "shell", path: "setup.sh"

end
