### Docker Use
You have docker installed on your machine and just have to run 
 - docker-compose up
 - It will run the server at port 4000.



 suppose your app is in a directory called myapp

A network called myapp_default is created.
 - A container is created using apache1’s configuration. It joins the network myapp_default under the name apache1.
 - A container is created using apache2’s configuration. It joins the network myapp_default under the name apache2.
 - A container is created using apache3’s configuration. It joins the network myapp_default under the name apache3. 
 - A container is created using nginx’s configuration. It joins the network myapp_default under the name nginx.
 - A container is created using db’s configuration. It joins the network myapp_default under the name db.

 Within the web container, your connection string to db would look like mysql://db:3306, and 
 from the host machine, the connection string would look like postgres://{DOCKER_IP}:3306.
 