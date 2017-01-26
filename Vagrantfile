Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.synced_folder '../src', '/mnt'
  config.vm.network "private_network", ip: "10.11.0.12"
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
  end
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant.yml"
  end
end

