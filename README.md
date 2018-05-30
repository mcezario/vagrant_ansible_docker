# Content

This example show how to create a virtual machine with docker installed.
<br/>
For the creation is used vagrant and ansible.

`Vagrant` create a `ubuntu/trusty64` virtual machine with `Ansible` plugin.
<br/>
`Ansible` contains a playbook with tasks that install docker

# Premise

You must have virtualbox and vagrant installed.

#### How to install virtualbox? <br/>
http://www.virtualbox.org/wiki/Downloads

#### How to install vagrant?<br/>
http://www.vagrantup.com/downloads.html

- In Linux, add `/opt/vagrant/bin` to your `PATH` variable.

Test the installation:
<br/>
`$` vagrant -v

> Example of install a `.deb` or `.rmp` file
>
> dpkg -i file.deb
>
> sudo rpm -i file.rpm


# Run the sample

Execute the command below for execute Vagrantfile. <br/>
`<repository> $` vagrant up

After execution, access the virtual machine by ssh. <br/>
`<repository> $` vagrant ssh vagrant_sample

Inside virtual machine, test the docker installation. <br/>
`vagrant@vagrant-ubuntu-trusty-64:~$` sudo docker -v

Result:
> Docker version 17.03.0-ce, build 3a232c8
