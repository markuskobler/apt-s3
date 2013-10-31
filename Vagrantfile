Vagrant.configure("2") do |config|
  config.vm.box     = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.provision "shell", inline: <<EOF
export DEBIAN_FRONTEND=noninteractive
sudo apt-get update
sudo -E apt-get -y -q install g++ devscripts debhelper cdbs binutils make libapt-pkg-dev libcurl4-openssl-dev
cd /vagrant
make
make deb
EOF
end
