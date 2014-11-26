FROM ubuntu:latest

MAINTAINER Nic Jackson <nicholas.jackson@marks-and-spencer.com>

# default exposed webserver port
EXPOSE 8000
EXPOSE 9090

# live refresh port for node
EXPOSE 35729

VOLUME /src

RUN sudo apt-get update

RUN sudo echo y | apt-get install git

RUN sudo echo y | apt-get install default-jre

# install ruby and SASS gem required to build SASS from grunt
RUN echo y | sudo apt-get install ruby
RUN echo y | sudo apt-get install ruby-dev
RUN echo y | sudo apt-get install build-essential
RUN gem install compass
RUN gem install bundler

RUN echo y | sudo apt-get install nodejs
RUN echo y | sudo apt-get install npm
RUN sudo ln -s /usr/bin/nodejs /usr/bin/node
RUN npm install -g bower
RUN npm install -g grunt-cli

CMD ["bash"]
