# docker-image

A Spring boot application is created from https://start.spring.io/ in JAVA. 
Packaged named as resource is created and in that a class is created in which GetMapping, RequestMapping  and RestController are present.
A Docker file is created named as Dockerfile in which type of application is defined. OpenJDK image is used as an image. Then jar file is added which is built by the application. Expose is used to expose the container on Port. Entry point is provided to give the jar name.

Then some commands need to be run at terminal. In order to create image , it should be build first and it is build via following commands:
docker build -f Dockerfile  -t docker-spring-boot .
It will create the image.
First it will download the openjdk image and it adds the jar into the container and then it will expose the port.
To check the image is create run following command:
docker images
It will give the image.
Now in order to run the particular image following command is run:
docker run -p 8085:8085 docker-spring-boot

Under application.properties add the port
Then at the browser go to port 8085 and hit the application.
