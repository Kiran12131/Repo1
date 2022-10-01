FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install openjdk-11-jdk wget
RUN mkdir /usr/local/tomcat
RUN wget https://dlcdn.apache.org/tomcat/tomcat-10/v10.0.26/bin/apache-tomcat-10.0.26.tar.gz -O /tmp/apache-tomcat-10.0.26.tar.gz
RUN cd /tmp && tar xvfz apache-tomcat-10.0.26.tar.gz
RUN cp -Rv /tmp/apache-tomcat-10.0.26/* /usr/local/tomcat/
EXPOSE 8080
#COPY **/*.war /usr/local/tomcat/webapps/qa.war
CMD /usr/local/tomcat/bin/catalina.sh run
