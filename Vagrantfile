Vagrant.configure("2") do |config|
    config.vm.define :sweb do |sweb|
      sweb.vm.box = "debian/bullseye64"
      sweb.vm.hostname = "sweb"
      sweb.vm.synced_folder ".", "/vagrant", disabled: true
      sweb.vm.network :private_network,
        :libvirt__network_name => "red1",
        :libvirt__dhcp_enabled => false,
        :ip => "10.0.0.100",
        :libvirt__forward_mode => "veryisolated"
    end
    config.vm.define :sdbase do |sdbase|
      sdbase.vm.box = "debian/bullseye64"
      sdbase.vm.hostname = "sdbase"
      sdbase.vm.synced_folder ".", "/vagrant", disabled: true
      sdbase.vm.network :private_network,
        :libvirt__network_name => "red1",
        :libvirt__dhcp_enabled => false,
        :ip => "10.0.0.101",
        :libvirt__forward_mode => "veryisolated"
    end
  end
