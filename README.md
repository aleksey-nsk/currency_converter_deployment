## Info

Task **Currency converter**. Detailed task requirements see in files/**task.pdf**.  
Project consists of repositories:  
- [Backend](https://github.com/aleksey-nsk/currency_converter_backend) 
- [Frontend](https://github.com/aleksey-nsk/currency_converter_frontend)
- Deployment (current repository)

## Deployment: run application in containers

1. Let's deploy the application in production. We will use **Docker containers**.  
   We need to run 3 containers:

       - PostgreSQL database  
       - Backend (Spring Boot REST API on embedded Tomcat-server)         
       - AngularJS-frontend on NGINX server  

2. Backend and frontend images were previously created and uploaded to **Docker Hub**:    
   ![](https://github.com/aleksey-nsk/currency_converter_deployment/blob/master/screenshots/01_1_docker_hub.png)  
   
3. Running file docker/**docker-compose.yaml** looks like this:    
   ![](https://github.com/aleksey-nsk/currency_converter_deployment/blob/master/screenshots/02_1_file_for_run.png)  
   ![](https://github.com/aleksey-nsk/currency_converter_deployment/blob/master/screenshots/02_2_file_for_run.png)  

4. Take a machine with installed **Docker** and **docker-compose**. Copy to this machine
   file docker/**docker-compose.yaml**. Next, open the folder with this file in the terminal, and run
   the command `docker-compose up --build`. 
   
   After that, the necessary images will be downloaded, and then
   the application will be run in containers. To view information, use the commands:  
   `docker image ls`  
   `docker container ls -a`  
   `docker volume ls`  
   `docker network ls`  
   
5. The application is available in the browser at: http://localhost:8099/

6. API documentation is available at: http://localhost:8082/swagger-ui/index.html
