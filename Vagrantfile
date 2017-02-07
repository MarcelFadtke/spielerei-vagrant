# Mafa Start
Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "httpd" do |httpd|
    httpd.vm.box = "hashicorp/precise64"
    httpd.vm.network :private_network, ip: "10.0.0.10"
    httpd.vm.hostname = "httpd"
  end

  config.vm.define "tomcat" do |tomcat|
    tomcat.vm.box = "hashicorp/precise64"
    tomcat.vm.network :private_network, ip: "10.0.0.11"
    tomcat.vm.hostname = "tomcat"
  end 
end
# Mafa - Ende

# von ReMi - Start
#
#Vagrant.configure("2") do |config|
#  config.vm.provision "shell", inline: "echo Hello"
# 
#  config.vm.define "httpd" do |httpd|
#    httpd.vm.box = "hashicorp/precise64"
#               httpd.vm.network "private_network", type: "dhcp"
#               httpd.vm.hostname = "httpd"
#               httpd.vm.synced_folder "../local_web", "/vagrant_data"
#               httpd.vm.provision :shell, path: "bootstrap.sh"
#               httpd.vm.network :forwarded_port, guest: 80, host: 80
#               httpd.vm.provision "shell", inline: <<-SHELL
#     apt-get update
#     apt-get install -y apache2
##             echo "ProxyPass / http://0.0.0.0:8080/" >> /etc/apache2/httpd.conf
##             echo "ProxyPassReverse / http://0.0.0.0:8080/"" >> /etc/apache2/httpd.conf
#   
#               SHELL
#  end
# 
#  config.vm.define "app" do |app|
#    app.vm.box = "hashicorp/precise64"
#               app.vm.network "private_network", type: "dhcp"
#               app.vm.hostname = "app"
#               app.vm.synced_folder "../local_tomcat", "/vagrant_data" 
#               app.vm.network :forwarded_port, guest: 8080, host: 8080
#               app.vm.provision "shell", inline: <<-SHELL
#                              apt-get update
#                              apt-get install -y default-jdk tomcat7
#               SHELL
#  end
# 
#  config.vm.provision "shell", inline: <<-SHELL
#               apt-get install -y avahi-daemon libnss-mdns
#  SHELL
#end
#
# von ReMi - Ende
