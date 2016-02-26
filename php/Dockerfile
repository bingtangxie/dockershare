FROM cariden/centos6.7
RUN rpm -ivh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN yum -y install php php-fpm
RUN sed -i '/^listen =/c\listen = 0.0.0.0:9000' /etc/php-fpm.d/www.conf
RUN sed -i '/^listen.allowed/c\;listen.allowed_clients = 127.0.0.1' /etc/php-fpm.d/www.conf
RUN mkdir -p /usr/share/nginx/html
EXPOSE 9000
CMD ["/usr/sbin/php-fpm"]
