# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Utilisation d'AlmaLinux 9 (Un clone bit-à-bit parfait de Red Hat Enterprise Linux 9, gratuit et idéal pour l'apprentissage)
  config.vm.box = "almalinux/9"

  # Machine 1 : Le Frontend (Reverse Proxy Nginx)
  config.vm.define "proxy" do |proxy|
    proxy.vm.hostname = "proxy.labs.local"
    proxy.vm.network "private_network", ip: "192.168.56.10"
    proxy.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
      vb.name = "N3_Projet1_Proxy"
    end
  end

  # Machine 2 : Le Backend (Le serveur Applicatif)
  config.vm.define "app" do |app|
    app.vm.hostname = "app.labs.local"
    app.vm.network "private_network", ip: "192.168.56.11"
    app.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
      vb.name = "N3_Projet1_App"
    end
  end

  # Machine 3 : La Base de données (PostgreSQL) et Serveur de stockage (NFS)
  config.vm.define "db" do |db|
    db.vm.hostname = "db.labs.local"
    db.vm.network "private_network", ip: "192.168.56.12"
    db.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
      vb.name = "N3_Projet1_DB"
    end
  end
end
