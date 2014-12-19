Vagrant LAMP
============

Want to test a new web app but don't want to affect your current Apache / MySQL / PHP system?
Applications like MAMP are great, but they don't make it easy to maintain multiple, separate
web roots.

If you find yourself needing quick to configure web stack, but also one that is customizable try this Vagrant project

Vagrant allows for Virtual Machines to be quickly setup, and easy to use.

And this project aims to make it very easy to spinup a complete LAMP stack in a matter of minutes.

Requirements
------------
* VirtualBox <http://www.virtualbox.com>
* Vagrant <http://www.vagrantup.com>
* Git <http://git-scm.com/>

Usage
-----

### Startup
	$ git clone https://github.com/slier81/vagrant-lamp.git
	$ cd vagrant-lamp
	$ vagrant up

That is pretty simple.

### Connecting

#### Apache
The Apache server is available at <http://localhost>

#### MySQL
Externally the MySQL server is available at port 8889, and when running on the VM it is available as a socket or at port 3306 as usual.
Username: root
Password: root

#### PhpMyadmin
PhpMyadmin is available at <http://localhost/phpmyadmin>
Username: root
Password: root

Technical Details
-----------------
* Ubuntu 14.04 64-bit
* Apache 2
* PHP 5.5 (xdebug preconfigured, worked out of the box)
* Composer
* MySQL 5.5
* Mailcatcher (preconfigured, worked out of the box)

We are using the base Ubuntu 14.04 box from Vagrant. If you don't already have it downloaded
the Vagrantfile has been configured to do it for you. This only has to be done once
for each account on your host computer.

The web root is located in the project directory at `www` and you can install your files there

And like any other vagrant file you have SSH access with

	$ vagrant ssh
