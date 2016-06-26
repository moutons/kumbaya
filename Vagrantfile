# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network :private_network, ip: '10.42.42.10'

  config.vm.provision "shell", inline: <<-SHELL

    # Apply the latest OS updates
    sudo apt-get update
    sudo apt-get upgrade

    # Install Python goodies
    sudo apt-get install --assume-yes python-pip
    sudo pip  install flask
    sudo pip  install flask-login
    sudo pip  install flask-openid
    sudo pip  install flask-mail
    sudo pip  install flask-sqlalchemy
    sudo pip  install sqlalchemy-migrate
    sudo pip  install flask-whooshalchemy
    sudo pip  install flask-wtf
    sudo pip  install flask-babel
    sudo pip  install guess_language
    sudo pip  install flipflop
    sudo pip  install coverage

    echo -e "Do the following from the vagrant vox as root:\nexport FLASK_APP=/vagrant/run.py\nexport FLASK_DEBUG=1\npython -m flask run --host=0.0.0.0"
  SHELL

end