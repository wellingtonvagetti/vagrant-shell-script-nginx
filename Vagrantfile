Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "forwarded_port", guest: 80, host: 8090
  config.vm.network "public_network", ip: "192.168.1.200"
  config.vm.synced_folder "site/", "/var/www/html"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "ubuntu-cep"
  end
  config.vm.provision "shell", path: "script.sh"
end