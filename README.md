# Process

1. Install prerequisites
  1. Download & install Vagrant (http://www.vagrantup.com/downloads.html)
  1. Download & install VirtualBox (https://www.virtualbox.org/wiki/Downloads)
  1. `gem install puppet`
  1. `gem install librarian-puppet`
1. Change into Puppet development working directory
1. Initialize Puppet Librarian
  1. `librarian-puppet init`
1. Update Puppetfile w/ required modules
1. Install modules
  1. `librarian-puppet install`

# Details

## Install VirtualBox

Vagrant can work with VirtualBox, AWS, VMware & some other hypervisors, but VirtualBox is freely available and thus used in this demo.  Be sure you have a current version of VirtualBox installed (4.3.8 as of this writing).  VirtualBox can be downloaded from https://www.virtualbox.org/wiki/Downloads.

## Install Vagrant

Vagrant can be downloaded & installed as a pre-built binary installer from
http://www.vagrantup.com/downloads.html.  Choose the package that is correct
for your operating system.  This demo requires a current version (v1.5.1 as of
this writing) to work.

## Install Gems

This demo utilizes librarian-puppet to manage the modules used.  For more
information on librarian-puppet, see https://github.com/rodjek/librarian-puppet.
librarian-puppet requires the following gems to be installed:

  ~~~ sh
  $ gem install puppet
  $ gem install librarian-puppet
  ~~~

## Initialize librarian-puppet

Note, this step is only necessary for new projects.  This demo has already
initialized librarian-puppet so this step isn't necessary.

1. Change into the `puppet-demo` directory you checked out (you're probably already here!)
1. Initialize librarian-puppet:

  ~~~ sh
  $ librarian-puppet init
  ~~~

## Manage Puppet Modules

Add any necessary Puppet modules by editing the `Puppetfile`.  Once changes
have been made, install them with librarian-puppet:

  ~~~ sh
  $ librarian-puppet install
  ~~~
