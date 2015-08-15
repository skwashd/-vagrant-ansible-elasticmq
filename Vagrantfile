# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty32"
  config.vm.network "private_network", ip: "192.168.33.13"
  config.vm.hostname = "elasticmq"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "elasticmq"
    vb.memory = 512
    vb.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
    ansible.sudo = true
    ansible.ask_sudo_pass = false

    ansible.playbook = "provisioning/playbook.yml"
    ansible.inventory_path = "provisioning/inventory"

    ansible.limit = "elasticmq"

    ansible.extra_vars = {
      host_username: `whoami`
    }
  end

end
