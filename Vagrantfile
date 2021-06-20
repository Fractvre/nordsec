
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
    

  config.vm.provider "virtualbox" do |vb|
  end

  config.vm.define "main" do |main|
    main.vm.network "public_network", ip: "192.168.1.10"
    main.vm.hostname = "main"
    main.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "playbooks/all.yaml"
      ansible.verbose = true
      ansible.install = true
      ansible.limit = "main"
      ansible.inventory_path = "inventory/inventory.ini"
    end
  end  

  config.vm.define "node1" do |node|
    node.vm.network "public_network", ip: "192.168.1.20"
    node.vm.hostname = "node1"
    node.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "playbooks/all.yaml"
      ansible.verbose = true
      ansible.install = true
      ansible.limit = "node1"
      ansible.inventory_path = "inventory/inventory.ini"
    end
  end

  config.vm.define "node2" do |node|
    node.vm.network "public_network", ip: "192.168.1.30"
    node.vm.hostname = "node2"
    node.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "playbooks/all.yaml"
      ansible.verbose = true
      ansible.install = true
      ansible.limit = "node2"      
      ansible.inventory_path = "inventory/inventory.ini"     
    end
  end

  config.vm.define "node3" do |node|
    node.vm.network "public_network", ip: "192.168.1.40"
    node.vm.hostname = "node3"
    node.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "playbooks/all.yaml"
      ansible.verbose = true
      ansible.install = true
      ansible.limit = "node3"      
      ansible.inventory_path = "inventory/inventory.ini"     
    end
  end
end
