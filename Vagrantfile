Vagrant.configure("2") do |config|

config.vm.provision "shell",path:"backup_script.sh"
config.vm.provision "shell",path:"lab1_p1.sh"
config.vm.provision "shell",path:"lab2_p2.sh"

  config.vm.define "box1" do |box1|

         box1.vm.box="ubuntu/trusty64"

         box1.vm.network :forwarded_port, guest: 22, host: 10122, id: "ssh" 

         box1.vm.network :private_network, ip: "192.168.56.101" 

         box1.vm.provider :virtualbox do |v| 
 
         v.customize ["modifyvm", :id, "--memory", 1020]

	   end
	end
  config.vm.define "box2" do |box2|

        box2.vm.provision "shell", path: "backup_script.sh"
                 #sudo apt-get install -y nginx

                 #SHELL

         box2.vm.box="puphpet/ubuntu1404-x64" 

         box2.vm.network :forwarded_port, guest: 22, host: 10223, id: "ssh"

         box2.vm.network :private_network, ip: "192.168.56.102"

      end

end





