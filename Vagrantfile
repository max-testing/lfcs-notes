Vagrant.configure("2") do |config|
  config.vm.define "lfcs" do |lfcs|
    # type and hostname
    lfcs.vm.box = "bento/centos-7.4"
    lfcs.vm.hostname = 'lfcs'
    
    # network
    lfcs.vm.network :private_network, ip: "192.168.57.101"
    lfcs.vm.network :forwarded_port, guest: 22, host: 10122, id: "ssh"
  end

  config.vm.provider "virtualbox" do |v|
    v.cpus = 2
  end
end
