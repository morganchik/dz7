FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y default-jdk
RUN apt-get install -y wget
RUN mkdir -p /temp01
RUN wget -O /temp01/tomcat-8.5.50.tar.gz https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/8.5.50/tomcat-8.5.50.tar.gz
RUN tar xvf temp01/tomcat-8.5.50.tar.gz -C temp01
RUN mv /temp01/apache-tomcat-8.5.50 /usr/local/tomcat
RUN chmod a+x /usr/local/tomcat/bin/*
EXPOSE 8080
CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]