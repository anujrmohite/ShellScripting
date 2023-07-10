rwxr-xr-x

Box -> Operating System Image

## vagrant box add USER/BOX

## vagrant box add jasonc/centos7

many public boxes to download

Vagrant project = folder with a vagrant file

## mkdir vm1

## cd vm1

now init the vagrant project

## vagrant init jasonc/centos7

## vagrant up

vm is started is headless mode -> no ui available

## vagrant up [VM_Name]

## vagrant up master

## vagrant up server1

## vagrant shh [VM_Name]

## exit

## vagrant halt [VM]

## vagrant up

## vagrant suspend

## vagrant resume

## vagrant destroy

## vagrant

Vagrant.configure (2) do config|
    config.vm.box= "jasonc/centos7"
    config.vm.hostname = "linuxsvrl"
    config.vm.network "private_network", ip: "10.2.3.4"
    config.vm.provider "virtualbox" do vb
    config.vm.provision "shell",path: "setup.sh"
        vb.gui = true
        vb.memory = "1024"
    end
end

Vagrant.configure (2) do |config|
    config.vm.box = "jasonc/centos7"

    config.vm.define "serverl" do server1|
        server1.vm.hostname = "server1"
        server1.vm.network "private_network", ip: "10.2.3.4"
    end

    config.vm.define "server2" do server2|
        server2.vm.hostname = "server2"
        server2.vm.network "private_network", ip: "10.2.3.5"
    end
end

## vagrant init
