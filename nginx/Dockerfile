FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install nginx -y
EXPOSE 80
ENV dir=/var/www/html
ARG app_type
COPY $app_type.html $dir/index.html
ADD http://18.224.200.108:32771/logo.png $dir/logo.png
CMD ["nginx","-g","daemon off;"]
WORKDIR $dir
RUN chmod 644 *

#docker build -t lab:prod --build-arg app_type=prod
#docker build -t lab:nonprod --build-arg app_type=non
