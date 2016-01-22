# ansible

- add 127.0.0.1 $HOSTNAME to /etc/hosts
- sudo apt-get update
- wget https://raw.githubusercontent.com/jinsenglin/screen/dev/.screenrc
- install docker
- install jenkins
 
# about install jenkins
- https://wiki.jenkins-ci.org/display/JENKINS/Installing+Jenkins+on+Ubuntu
- wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
- sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'
- sudo apt-get update
- sudo apt-get install jenkins
- sudo service jenkins start

# about install docker
- https://docs.docker.com/engine/installation/ubuntulinux/
- sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
- sudo echo "deb https://apt.dockerproject.org/repo ubuntu-trusty main" > /etc/apt/sources.list.d/docker.list
- sudo apt-get update
- sudo apt-get purge lxc-docker
- sudo apt-cache policy docker-engine
- sudo apt-get upgrade
- sudo apt-get update
- sudo apt-get install linux-image-extra-$(uname -r)
- sudo apt-get install docker-engine
- sudo service docker start
