Vagrant.configure(2) do |config|

  config.vm.box = "debian/jessie64"
  config.ssh.insert_key = false

  config.vm.network "forwarded_port", guest: 80, host: 9090
  config.vm.hostname = "adminotaur.dev"
  
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook-auto.yml"
  end
end
