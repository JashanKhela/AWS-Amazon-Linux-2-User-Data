# AWS-Amazon-Linux-2-User-Data
This is a script created for an Apache server to be set up on an EC2 instance.

######
#!/bin/bash

##################### USE THIS FILE IF YOU LAUNCHED AMZOJ LINUX 2 #########################

######GET ADMIN PRIVILEDGES ########
sudo su 

####### install httpd (Linux 2 version) ########
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo "Hello World from $(hostname -f)" > var/www/html/index.html

