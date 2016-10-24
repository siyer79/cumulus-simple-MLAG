Vagrant.configure(2) do |config|

   config.vm.box = "cumulus-vx-3.1.1"

   
##### DEFINE VM for leaf-1 #####
   config.vm.define "leaf-1" do |device|
     device.vm.hostname = "leaf-1"
     device.vm.network "private_network", virtualbox__intnet: "swp1"
     device.vm.network "private_network", virtualbox__intnet: "swp2"
     device.vm.network "private_network", virtualbox__intnet: "swp3"
     device.vm.network "private_network", virtualbox__intnet: "swp4"
     device.vm.network "private_network", virtualbox__intnet: "swp5"
     device.vm.network "private_network", virtualbox__intnet: "swp6"

     device.vm.provider "virtualbox" do |v|
       v.name = "leaf-1"
       v.memory = 512
     end

   end

##### DEFINE VM for leaf-2 #####
   config.vm.define "leaf-2" do |device|
     device.vm.hostname = "leaf-2"
     device.vm.network "private_network", virtualbox__intnet: "swp1"
     device.vm.network "private_network", virtualbox__intnet: "swp2"
     device.vm.network "private_network", virtualbox__intnet: "swp3"
     device.vm.network "private_network", virtualbox__intnet: "swp4"
     device.vm.network "private_network", virtualbox__intnet: "swp5"
     device.vm.network "private_network", virtualbox__intnet: "swp6"

     device.vm.provider "virtualbox" do |v|
       v.name = "leaf-2"
       v.memory = 512
     end

   end


   config.vm.provision "ansible" do |ansible|
     ansible.verbose = "vvv"
     ansible.playbook = "dell-leaf-playbook.yml"
   end


end



