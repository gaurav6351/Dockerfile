FROM gaurav04/centos-httpd-php:v1
RUN yum -y update && \
	yum -y install wget && \
	yum -y install tar 
 
RUN yum -y install java-1.7.0-openjdk.x86_64
 
RUN mkdir /home/inv
WORKDIR /home/inv
RUN wget http://archive.apache.org/dist/tomcat/tomcat-8/v8.0.30/bin/apache-tomcat-8.0.30.tar.gz
RUN tar -xvf apache-tomcat-8.0.30.tar.gz

ADD tomcat.sh /tmp

WORKDIR /tmp

EXPOSE 80
EXPOSE 8080

CMD ["./tomcat.sh"]
