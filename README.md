# Jenkins_Multibranch_Pipeline

### Run Jenkins in Docker Container

`docker pull jenkins/jenkins`

`docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts`

1. Get the password show in the terminal for initialising
2. After that install suggested plugins
