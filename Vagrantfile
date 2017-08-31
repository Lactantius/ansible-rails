Vagrant.configure("2") do |config|

  config.vm.network "private_network", ip: "192.168.144.1"

  config.vm.define :centos do |machine|
    machine.vm.box =      "centos/7"
    machine.vm.hostname = "centos-rails"
    
    machine.vm.provider :libvirt do |domain|
      domain.memory = 1024
      domain.cpus = 1
    end

    # machine.vm.provision "ansible" do |ansible|
    #   ansible.verbose = "v"
    #   ansible.playbook = "provisioning/site.yml"
    #   ansible.limit = "all"
    #   ansible.groups = {
    #     "rails-server" => [ "centos-rails" ]
    #   }
    # end

  end

end
