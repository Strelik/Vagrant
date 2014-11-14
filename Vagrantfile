# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"








Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.












  # Every Vagrant virtual environment requires a box to build off of. Define it here. 
  config.vm.box = "CentOS_Minimal7"









  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false
  

  
  
  #Virtual Machine Name
  config.vm.provider "virtualbox" do |v|
  v.name = "Vagrant_Test_VM"
  end




  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080




  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  config.vm.network "public_network"




  # If true, then any SSH connections made will enable agent forwarding.
  # Default value: false
  # config.ssh.forward_agent = true







  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"








  # Uncomment here to provide a GUI when the VM boots up.
  # config.vm.provider "virtualbox" do |vb|
  #   # Don't boot with headless mode
  #   vb.gui = true
 
 
 
 
 
  #   # Use VBoxManage to customize the VM. For example to change memory:
  #   vb.customize ["modifyvm", :id, "--memory", "1024"]
  # end





  
  #Supposed to be able to specify your public bridge if you have more than one bridgable interface here. 
  Vagrant.configure("2") do |config|
  config.vm.network "public_network", bridge: 'p117p1'
  end



 

  #Shortcut to have VirtualBox Allocate CPU and RAM
  config.vm.provider "virtualbox" do |v|
  v.memory = 4096
  v.cpus = 2
  end




  #Initial Config Provision Block
  config.vm.provision "shell" do |s|
    s.inline = "echo Hello, Let Us Begin To Provision!"
  end

  #Basic Ansible Provisioning Block Asking For Sudo Permission
  config.vm.provision "ansible" do |ansible|
    ansible.sudo = true
    ansible.playbook = "provisioning/main.yml"
  end

    
  

end
