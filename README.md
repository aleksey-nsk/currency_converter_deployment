# Info

Тестовое задание **Конвертер валют**. Подробное условие в файле files/**task.pdf**.  
Проект состоит из репозиториев:
- [Backend](https://github.com/aleksey-nsk/currency_converter_backend) 
- [Frontend](https://github.com/aleksey-nsk/currency_converter_frontend)
- Deployment (данный репозиторий)

## Deployment: запустить приложение в контейнерах

1. Развернём приложение в проде. Будем использовать **Docker-контейнеры**. Поднимем 3 контейнера:

       - База данных PostgreSQL
       - Бэкенд (Spring Boot REST API на встроенном Tomcat-сервере)       
       - AngularJS-фронтенд на сервере NGINX

2. Образы для бэкенда и фронтенда уже созданы и загружены на **Docker Hub**:  
   ![](https://github.com/aleksey-nsk/currency_converter_deployment/blob/master/screenshots/01_1_docker_hub.png)  
   
3. Файл для запуска docker/**docker-compose.yaml** выглядит так:  
   ![](https://github.com/aleksey-nsk/currency_converter_deployment/blob/master/screenshots/02_1_file_for_run.png)  
   ![](https://github.com/aleksey-nsk/currency_converter_deployment/blob/master/screenshots/02_2_file_for_run.png)  

4. Возьмите машину, на которой установлены **Docker** и утилита **docker-compose**. Скопируйте на эту машину
   файл docker/**docker-compose.yaml**. Далее откройте в терминале папку с этим файлом и выполните
   команду `docker-compose up --build`. После этого скачаются нужные образы, создадутся контейнеры, и затем
   приложение будет запущено в контейнерах. Для просмотра информации использовать команды:    
   `docker image ls`  
   `docker container ls -a`  
   `docker volume ls`  
   `docker network ls`  
   
5. Приложение доступно в браузере по адресу: http://localhost:8099/

6. Документация к API доступна по адресу: http://localhost:8082/swagger-ui/index.html
