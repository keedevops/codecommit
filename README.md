wget https://downloads.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz
mkdir /etc/tomcat
sudo mkdir /etc/tomcat
sudo tar -xf apache-tomcat-9.0.83.tar.gz -C /etc/tomcat/
sudo chown ubuntu:ubuntu /etc/tomcat/ -R
sudo chmod +x /etc/tomcat/apache-tomcat-9.0.83/bin/*.sh

