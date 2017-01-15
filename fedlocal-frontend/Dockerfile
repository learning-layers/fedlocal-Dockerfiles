FROM learninglayers/base

MAINTAINER Dominik Renzel

RUN apt-get update
RUN apt-get install -y \
                     wget \
                     unzip

WORKDIR /var/www

# Download & unpack las2peer service CI build from Jenkins
RUN wget http://layers.dbis.rwth-aachen.de/jenkins/job/las2peer-Demo-Service/lastSuccessfulBuild/artifact/*zip*/archive.zip \
&& unzip archive.zip \
&& rm archive.zip \
&& mv archive/frontend /var/www/fedlocal \
&& rm -rf archive

VOLUME ["/var/www/fedlocal/"]

