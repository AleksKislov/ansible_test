Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  
  # прокидываю порты для обоих веб серверов 
  config.vm.network "forwarded_port", guest: 80, host: 8080  # для Nginx
  config.vm.network "forwarded_port", guest: 8080, host: 8081  # для Apache

  # private network для ансибл 
  config.vm.network "private_network", ip: "192.168.56.10"
end
