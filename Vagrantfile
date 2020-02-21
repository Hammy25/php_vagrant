# Vagrant configuration
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  # Network configuration
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Private network
  config.vm.network "private_network", ip: "192.168.33.10"

  # Shared folder settings
  config.vm.synced_folder "./website", "/var/www/html/", owner:"www-data", group:"www-data"
  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provider "virtualbox" do |vb|
     # Display the VirtualBox GUI when booting the machine
     vb.gui = true
  
     # Customize the amount of memory on the VM:
     vb.memory = "1024"
  end
  
  config.vm.provision "shell", path:"install.sh"
end
