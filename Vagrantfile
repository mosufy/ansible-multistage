# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "bento/centos-7.2"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.network "private_network", ip: "10.8.8.88"

  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"

  config.vm.synced_folder "./", "/var/www/ansible-multistage", :nfs => { :mount_options => ["dmode=777","fmode=777"] }

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.customize ["modifyvm", :id, "--cableconnected1", "on"]
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "ansible/site.yml"
    ansible.inventory_path = "ansible/inventories/dev/hosts.ini"
    ansible.limit = 'all'
  end

end