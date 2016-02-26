FROM cariden/centos6.7
RUN rpm -ivh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN yum -y install nginx
COPY default.conf /etc/nginx/conf.d/default.conf
COPY fastcgi_params /etc/nginx/fastcgi_params
EXPOSE 80
CMD ["/usr/sbin/nginx","-g","daemon off;"]
