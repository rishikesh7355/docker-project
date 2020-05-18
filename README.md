# docker-project

Docker : It is set of PAAS(platform as a service )products for  creating and deploying images as anywhere very fastly using container technology 

Docker Mutli -tier Infrastructure 

Pre-requisites    :
The following terms and technology should be known - 

red hat linux (RHEL8) system installed
Linux commands like mkdir ,ls ,volume,vim or gedit text editors ,about systemctl and networking commands etc 

yum or dnf packages preinstalled


docker :
 docker images like mysql 5.7 and wordpress which are used in this project
 how to pull and run images 
 docker commands like run ,exec ,pull ,start,stop ,etc.
 Entrypoint concepts 
 
 
 Docker -Compose :
 
 used for making Infrastucture as code 
 some syntax concepts of how to write YAML scripts 
 
 First :pull images 
 1.docker pull mysql :5.7
 -- Now we have to launch and make account on mysql database 
 for this goto image description on dockerhub.com for entrypoint scripts 
 -- check all environmental variables
 --also to create all data permament create a separate folder 
 2.docker volume create mysql_storage 
 
 
 ![Screenshot (33)_LI](https://user-images.githubusercontent.com/54662528/82225264-9d0d3080-9942-11ea-88d2-7f2651893b8f.jpg)
 
