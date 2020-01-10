#Docker file for apache for demoapp
#docker pull gets called to run FROM 
FROM centos:7
MAINTAINER solanki.sapna30@gmail.com
RUN yum -y update
RUN yum -y install httpd php php-gd php-mysql
#ADD scripts /opts
#RUN chmode 755 /opts/*
#RUN /opts/packages
ADD code /var/www/html
#COPY code/* /var/www/html
ENV MY_DB_HOST_WRITE=test
EXPOSE 80
#Instead of CMD if ENTRYPOINT given, it can't be overwritten at runtime
# CMD will be executed with Sh -C command same as run and hence json array needs to be created for having CMD
CMD ["httpd", "-D" ,"FOREGROUND"]