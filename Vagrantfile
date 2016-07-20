# vagrant box with docker
#
Vagrant.configure(2) do |config|
  config.vm.define :u14docker do |node|
    node.vm.hostname = "u14docker"
    node.vm.box = "ubuntu/trusty64"
    node.vm.network :private_network, :ip => "192.168.33.99"
    node.vm.provider :virtualbox do |domain|
      domain.memory = 1024
      domain.cpus = 2
	  end

    # install docker
    node.vm.provision "ansible" do |ansible|
      ansible.playbook = "install_docker.yml"
    end
  end
end
