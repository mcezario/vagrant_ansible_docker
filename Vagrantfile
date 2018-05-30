VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.define :vagrant_sample do |vagrant_sample|
    vagrant_sample.vm.network :private_network, :ip => "192.168.33.10"

    #https://docs.ansible.com/ansible/2.5/scenario_guides/guide_vagrant.html#introduction
    #https://www.vagrantup.com/docs/provisioning/ansible_intro.html
    config.ssh.insert_key = false

    vagrant_sample.vm.provision :ansible do |ansible|
        ansible.verbose = "v"
        ansible.playbook = "playbook.yml"
    end

  end

end
