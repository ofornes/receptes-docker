FROM openjdk:8
WORKDIR /opt/app
ADD --chown=1000:1000 receptes-0.0.1.jar .
ADD --chown=1000:1000 application.yml .
EXPOSE 80 8080
ENTRYPOINT [ "java" ,"-jar", "receptes-0.0.1.jar" ]
