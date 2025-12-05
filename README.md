<img width="1920" height="1080" alt="Screenshot (352)" src="https://github.com/user-attachments/assets/e458c409-149d-432e-b769-851736c2145b" />
<img width="1920" height="1080" alt="Screenshot (351)" src="https://github.com/user-attachments/assets/2a253874-fe25-4505-9bd8-37aedd5a784d" />
<img width="1920" height="1080" alt="Screenshot (350)" src="https://github.com/user-attachments/assets/e8cc5eba-cdcb-4306-8717-c49d4b6b5093" />
<img width="1920" height="1080" alt="Screenshot (349)" src="https://github.com/user-attachments/assets/da692a37-84ed-4ee8-bd88-49ba1ad18771" />

######java-spring-boot-projrct-deployed-application######

###👉  Create an Amazon RDS Instance  👉 Click “Create database”

                                      👉 Choose a database engine -MySQL , full configuration
                                            
                                      👉 Choose version - MySQL 8.0.x
                                       
                                      👉 Choose a Template- Free tier (if eligible) , Dev/Test(Production)
        
                                      👉 Choose a Master username - admin 
  
                                      👉 Choose a Master password - self managed - Set a strong password.Confirm the password

                                      👉 Configure Instance Size - db t3.micro

                                      👉 Connectivity - vpc(default) , subnet group , security group

                                      👉 Choose a accessible - public
                                      
                                      👉 Choose Create Database 



##### create 2 EC2-Instance #####

 #👉 create ec2- docker-c7xi.large ,procced with keypair ,attach IAM role(ec2-fullaccess), security group

     
   #👉 connect ec2-  👉 sudo su -
  
                     👉 yum install docker -y
 
                     👉 systemctl start docker 

                     👉 systemctl enable  docker

                     👉 yum install git -y

                     👉 git clone https://github.com/Samir-CloudAwswithDevops/Java-springboot-project-1.git

                     👉 ls cd Java-springboot-project-1 ls 
 
                     👉 cd backend   # vi dockerfile

                     👉 vi docker file inside # change rds <endpoint> password :wq!
   
                     👉 cd backend - docker build -t backend .

                     👉 cd backend - docker run -dt -p 8084:8080 backend 

                      # leave this backend part hit publicip-port 8084

   
👉 cd frontend     👉 cd frontend inside - # vi dockerfile # change ec2 private ip:8082

                    👉 cd frontend inside - # vi requirement.text # add plotly

                    👉 cd frontend - docker build -t frontend .
                   
                    👉 cd frontend - docker run -dt -p 8502:8501 frontend

                    👉 cd frontend - docker ps

                    👉 cd frontend - docker images

                     # copy publicip:8502 hit brower 🎉 Deployment Complete!

