Vagrant.configure("2") do |config|
  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/trusty64"
    web.vm.hostname = 'web'
    web.vm.box_url = "ubuntu/trusty64"

    web.vm.network :public_network, ip: "192.168.1.100"

    web.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 512]
      v.customize ["modifyvm", :id, "--name", "web"]
    end
  end

  # config.vm.define "db" do |db|
  #   db.vm.box = "ubuntu/trusty64"
  #   db.vm.hostname = 'db'
  #   db.vm.box_url = "ubuntu/trusty64"
  #
  #   db.vm.network :public_network, ip: "192.168.1.111"
  #
  #   db.vm.provider :virtualbox do |v|
  #     v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  #     v.customize ["modifyvm", :id, "--memory", 512]
  #     v.customize ["modifyvm", :id, "--name", "db"]
  #   end
  # end
end
