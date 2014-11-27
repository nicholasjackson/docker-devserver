FROM ubuntu:latest

MAINTAINER Nic Jackson <nicholas.jackson@marks-and-spencer.com>

# default exposed webserver port
EXPOSE 8000
EXPOSE 9090
EXPOSE 9000
EXPOSE 9001

# live refresh port for node
EXPOSE 35729

VOLUME /src

RUN sudo apt-get update

# install git
RUN sudo echo y | apt-get install git

# install java
RUN sudo echo y | apt-get install default-jre

# install xvfb
RUN echo y | sudo apt-get install xfonts-100dpi xfonts-75dpi xfonts-scalable xfonts-cyrillic
RUN echo y | sudo apt-get install xvfb
RUN echo y | sudo apt-get install firefox

# install ruby and SASS gem required to build SASS from grunt
RUN echo y | sudo apt-get install ruby
RUN echo y | sudo apt-get install ruby-dev
RUN echo y | sudo apt-get install build-essential
RUN gem install compass
RUN gem install bundler

# install node and dependencies
RUN echo y | sudo apt-get install nodejs
RUN echo y | sudo apt-get install npm
RUN sudo ln -s /usr/bin/nodejs /usr/bin/node
RUN npm install -g bower
RUN npm install -g grunt-cli

CMD ["bash"]
