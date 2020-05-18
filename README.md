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
 
 
-- Now, rum the coomand as shown to launch the container name as dbos


3.docker ps ( # to check the running container names )
 
 ![Annotation 2020-05-18 205843](https://user-images.githubusercontent.com/54662528/82232376-2ffe9880-994c-11ea-811d-b263d74c66fe.png)
 
 
 4.docker exec -it dbos bash (# to go inside container dbos)
 
show databases ; (#to see database is created )

exit ;



![Annotation 2020-05-17 221004](https://user-images.githubusercontent.com/54662528/82235993-157aee00-9951-11ea-9d6f-4afd319fe865.png)



Similary,

-- goto dockerhub.com to check th environmental variables for image wordpress 

-- wordpress is apache websever used for creating blogs and dynamic webpages 
 
 -- create a separate storage for keeping data permanent 
 
 --  we need to create  the DNS link between mysql database and wordpress hosts
 
-- for this we need to configure webserrver and php but wordpress image already has this requirements


  
  6.docker volume create wp_storage 
  
  now run the commands as shown below to launch the container name as wpos 
 


![Annotation 2020-05-18 210102](https://user-images.githubusercontent.com/54662528/82232251-ffb6fa00-994b-11ea-8ff1-c7501392774a.png)


 -- Now at last we need to install Docker-compose
 
-- To keep the monitoring ,scaling ,testing of both the containers in a single go to reduce manual works and instead of launching and starting the conatainers again and again  we can use  docker -compsoe

--DOCKER-COMPOSE : it is a infrasturcture as a code because we are coding using YAML file format instead of manual works

--Goto dockerhub < search for linux version of docker-compose <copy the command and paste on terminal to install docker compose 

--make a seperate directory for writing YAML file
  
  7.mkdir mycompose 
  
  -- Go inside this folder
  
  8.vim docker-compose.YML
  
  --vim is text editor
  
  --press i to insert 
  
  --esc to come out of insert mode 
  
  --:wq to exit 
  
  -- NOTE : YAML file format uses syntax somewhat like python so mind the spaces 
  
  --Now write all codes as shown below in single file not seperate my screenshots are seperate not yaml file 
   
  

![Annotation 2020-05-17 235125](https://user-images.githubusercontent.com/54662528/82236183-625ec480-9951-11ea-9cd3-1eadee057df5.png)



![Annotation 2020-05-17 235252](https://user-images.githubusercontent.com/54662528/82236192-65f24b80-9951-11ea-9c98-c5ed0a5bc76d.png)








![Annotation 2020-05-17 215405](https://user-images.githubusercontent.com/54662528/82236226-6e4a8680-9951-11ea-8b13-a87cd8fd103d.png)



![Annotation 2020-05-17 215534](https://user-images.githubusercontent.com/54662528/82236258-77d3ee80-9951-11ea-9f0a-898eac8fc9cd.png)









