Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = "1024"
    v.cpus = 2
    v.customize ["modifyvm", :id, "--cpuexecutioncap", "70"]
  end

  config.vm.define :testcli1 do |testcli1|
#   testcli1.vm.box = "bento/centos-6.10"
    testcli1.vm.box = "clouddood/RH7.5_baserepo"
    testcli1.vm.host_name = "testcli1.test.dev"

#   testcli1.vm.ssh.forward_agent = true

    testcli1.vm.provision "ansible" do |ansible|
      ansible.playbook = "deploy_testcli.yml"
      ansible.inventory_path = "vagrant_hosts"
#     ansible.tags = ansible_tags
#     ansible.verbose = ansible_verbosity
#     ansible.extra_vars = ansible_extra_vars
#     ansible.limit = ansible_limit
    end

#   testcli1.vm.network :private_network, ip: "10.0.1.26"
    testcli1.vm.network :private_network, ip: "192.168.60.148"
  end

  config.vm.define :testcli2 do |testcli2|
#   testcli2.vm.box = "bento/centos-6.10"
    testcli2.vm.box = "clouddood/RH7.5_baserepo"
    testcli2.vm.host_name = "testcli2.test.dev"

#   testcli2.ssh.forward_agent = true

    testcli2.vm.provision "ansible" do |ansible|
      ansible.playbook = "deploy_testcli.yml"
      ansible.inventory_path = "vagrant_hosts"
#     ansible.tags = ansible_tags
#     ansible.verbose = ansible_verbosity
#     ansible.extra_vars = ansible_extra_vars
#     ansible.limit = ansible_limit
    end

#   testcli2.vm.network :private_network, ip: "10.0.1.27"
    testcli2.vm.network :private_network, ip: "192.168.60.149"
  end

  config.vm.define :testcli3 do |testcli3|
#   testcli3.vm.box = "bento/centos-6.10"
    testcli3.vm.box = "clouddood/RH7.5_baserepo"
    testcli3.vm.host_name = "testcli3.test.dev"

#   testcli3.ssh.forward_agent = true

    testcli3.vm.provision "ansible" do |ansible|
      ansible.playbook = "deploy_testcli.yml"
      ansible.inventory_path = "vagrant_hosts"
#     ansible.tags = ansible_tags
#     ansible.verbose = ansible_verbosity
#     ansible.extra_vars = ansible_extra_vars
#     ansible.limit = ansible_limit
    end

#   testcli3.vm.network :private_network, ip: "10.0.1.28"
    testcli3.vm.network :private_network, ip: "192.168.60.150"
  end

#######################################################################################################################################

# config.trigger.before :destroy do |trigger|
#   run "rm -Rf /tmp/abc/*"
    # subscription-manager remove --all
    # subscription-manager unregister
    # subscription-manager clean
#   trigger.name = "Destroy Trigger ..."
#   trigger.info = "Destroy Trigger Execution ..."
#   trigger.run = { path: "subscription-manager remove --all"}
#   trigger.run = { path: "subscription-manager unregister"}
#   trigger.run = { path: "subscription-manager clean"}
# end
end

