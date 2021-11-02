# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "rootca" do |rootca|
    rootca.vm.box = "peru/windows-server-2012_r2-standard-x64-eval"
    rootca.vm.provider :libvirt do |domain|
      domain.memory = 1024
    end
    rootca.vm.hostname = "rootca"
    rootca.vm.network "private_network", ip: "192.168.33.2"
  end

  config.vm.define "subca" do |subca|
    subca.vm.box = "peru/windows-server-2012_r2-standard-x64-eval"
    subca.vm.provider :libvirt do |domain|
      domain.memory = 1024
    end
    subca.vm.hostname = "subca"
    subca.vm.network "private_network", ip: "192.168.33.3"
  end

  config.vm.define "dc" do |dc|
    dc.vm.box = "peru/windows-server-2012_r2-standard-x64-eval"
    dc.vm.provider :libvirt do |domain|
      domain.memory = 1024
    end
    dc.vm.hostname = "dc"
    dc.vm.network "private_network", ip: "192.168.33.10"
    # dc.vm.provision "ansible" do |ansible|
      # ansible.playbook = "dc-playbook.yml"
    # end
  end

  config.vm.define "sccm" do |sccm|
    sccm.vm.box = "peru/windows-server-2016-standard-x64-eval"
    sccm.vm.provider :libvirt do |domain|
      domain.memory = 4096
    end
    sccm.vm.hostname = "sccm"
    sccm.vm.network "private_network", ip: "192.168.33.20"
    # sccm.vm.provision "ansible" do |ansible|
      # ansible.playbook = "sccm-playbook.yml"
    # end
  end

  # config.vm.define "fsp" do |sccm|
    # fsp.vm.hostname = "sccm"
    # fsp.vm.network "private_network", ip: "192.168.33.30"
    # fsp.vm.provision "ansible" do |ansible|
      # ansible.playbook = "fsp-playbook.yml"
    # end
  # end


end
