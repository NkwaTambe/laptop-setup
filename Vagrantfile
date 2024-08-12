Vagrant.configure('2') do |config|
  (1..1).each do |i|
    config.vm.define "setup" do |machine|
      machine.vm.box = 'ubuntu/focal64'
      machine.vm.hostname = "setup"
      machine.vm.provider "virtualbox" do |vb|
        vb.name = "laptup-setup-#{i}"
        vb.cpus = '4'
        vb.memory = '2048'
      end

      # Provision the VM with a shell script
      machine.vm.provision "shell", path: "setup.sh"
    end
  end
end

