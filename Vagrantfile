# -*- mode: ruby -*-
# vi: set ft=ruby :

CENTOS6_INSTALL_PUPPET = <<EOF
sudo yum -q -y install https://yum.puppetlabs.com/el/6/products/x86_64/puppetlabs-release-6-7.noarch.rpm
sudo yum-config-manager --enable rhel-6-server-optional-rpms
sudo yum -q -y install puppet
EOF

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box_url = "http://developer.nrel.gov/downloads/vagrant-boxes/CentOS-6.4-i386-v20130731.box"
  config.vm.box = "CentOS-6.4-i386-v20130731"

  #config.vm.provision :shell, :inline => CENTOS6_INSTALL_PUPPET

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file  = "site.pp"
    puppet.module_path    = "modules"
  end

end
