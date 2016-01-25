# ansible

- add 127.0.0.1 $HOSTNAME to /etc/hosts
- sudo apt-get update
- wget https://raw.githubusercontent.com/jinsenglin/screen/dev/.screenrc
- install docker
- install jenkins
- install nginx
 
# about install jenkins
- https://wiki.jenkins-ci.org/display/JENKINS/Installing+Jenkins+on+Ubuntu
- wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
- sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'
- sudo apt-get update
- sudo apt-get install jenkins
- sudo service jenkins start
- http://stackoverflow.com/questions/17940612/authentication-error-in-jenkins-on-using-sudo
- sudo echo "jenkins ALL= NOPASSWD: ALL" >> /etc/sudoers
- firefox http://<IP>:8080/

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

# about helo-docker in jenkins
- sudo docker run hello-world

# about install nginx
- sudo apt-get install nginx
- firefox http://<IP>/

# about build docker image 'openstackc-cli'
- wget https://raw.githubusercontent.com/jinsenglin/docker/master/dockerfiles/ubuntu14.04.3-openstack-cli/Dockerfile
- sudo docker build -t openstack-cli .
 
# about install gitlab
- https://about.gitlab.com/upgrade-to-package-repository/
- curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | sudo bash
- sudo apt-get install gitlab-ce
- firefox http://<IP>/
