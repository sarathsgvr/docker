FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install openjdk-11-jdk wget tar -y
ADD http://mirror.23media.de/apache/tomcat/tomcat-8/v8.5.29/bin/apache-tomcat-8.5.29.tar.gz  /opt/tomcat/
WORKDIR /opt/tomcat
RUN tar -xzf apache-tomcat-8.5.29.tar.gz
WORKDIR /opt/tomcat/apache-tomcat-8.5.29/bin/
RUN chmod 777 startup.sh shutdown.sh catalina.sh
ADD https://tomcat.apache.org/tomcat-8.0-doc/appdev/sample/sample.war /opt/tomcat/apache-tomcat-8.5.29/webapps/
EXPOSE 8080
WORKDIR /opt/tomcat/apache-tomcat-8.5.29/ 
CMD bin/catalina.sh run
