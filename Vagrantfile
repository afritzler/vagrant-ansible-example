Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provision "ansible" do |ansible|
    ansible.groups = {
      "webservers" => ["192.168.33.10"],
      "all_groups:children" => ["webservers"]
    }
    ansible.playbook = "provisioning/playbook.yml"
  end
end
