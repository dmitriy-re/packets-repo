
Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

#  config.vm.provision "ansible" do |ansible|
#    ansible.verbose = "vvv"
#    ansible.playbook = "playbook.yml"
#    ansible.become = "true"
#  end

  config.vm.provider "virtualbox" do |v|
    v.memory = 512
    v.cpus = 1
  end

  config.vm.define "ex8" do |ex6|
    ex6.vm.network "private_network", ip: "192.168.50.10", virtualbox__intnet: "net1"
    ex6.vm.hostname = "ex6"
    ex6.vm.provision "shell", path: "ex6_script.sh"
  end


end
