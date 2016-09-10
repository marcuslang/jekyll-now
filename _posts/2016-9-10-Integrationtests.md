# Integrationtests made easy (and automated)

In the dark ages of software development those who wanted to test their pile of code against a database or remote systems had to put a lot of effort in that.
Building a VM from an image, installing all the stuff they needed and give to admin so it could be hosted on server, also hoping that no colleague would leave the VM in an unusable state.  
Nowadays we have it a lot easier than that. Thanks to our modern tools we can easily put together a VM with all the things we need for our own, test against it and than start all over in a proper time.
Nonetheless I still see sometimes colleagues fighting about the ownership of a VM or hesitate when it comes to do an integration test.
This is why I wrote this article.

## goal
What I want you to show is how to automate your integration testing with tools taking care of starting, preparing and cleaning VMs for you. At the end we will have a test that runs against a freshly installed PostGreSQL DB on a VM with all the data we needed in the DB.  
In order to achive that goal we will let
 * Vagrant control the VM
 * Ansible do the provision of the stuff we need on the VM (in this case a PostGreSQL DB)
 * Maven Exec start the VM before and stop the VM after the tests
 * Maven Failsafe run the tests

## setup
##### Vagrant:
[Vagrant](https://www.vagrantup.com/) needs to be installed on your system. It will also need a provider like [VirtualBox](https://www.virtualbox.org/) or [VMWare](http://www.vmware.com/)
##### Ansible:
Ansible will do the provision of the system. Since it lacks native support for Windows, we will let Vagrant install Ansible as a local provisioner on the VM. 
##### PostGreSQL


### integration test with maven failsafe
* start VM
* running tests
* stop VM and cleaning

### recap