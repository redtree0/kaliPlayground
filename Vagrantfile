# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 
  config.vm.define "playground" do |playground|
    playground.vm.box = "offensive-security/kali-linux"
    playground.vm.box_check_update = false
    playground.vm.provider "virtualbox" do |vb|
      # Display the VirtualBox GUI when booting the machine
      # vb.gui = false
      vb.gui = true
      vb.memory = "3072"
      vb.cpus = "4"
      # vb.memory = "2048"
      # vb.cpus = "2"
    end
    playground.vm.network "private_network", ip: "192.168.99.20"
    
    
    # Provision the machine with a shell script
    playground.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y crowbar python3 python3-pip python3-apt
    SHELL

  end

end
