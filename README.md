# Jenkins_Multibranch_Pipeline

### 1. Run Jenkins in Docker Container

`docker pull jenkins/jenkins`

`docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts`

<img width="656" alt="image" src="https://user-images.githubusercontent.com/77828396/221528020-b6eb8ea5-4201-4461-ad04-85982900962f.png">


1. Get the password show in the terminal for initialising
2. After that install suggested plugins

<img width="666" alt="image" src="https://user-images.githubusercontent.com/77828396/221528148-2230540a-cdaf-4aa7-b87f-410238d1475d.png">

3. Create job type Multibranch Pipeline and add the credintioals and repo url and run

3. Create file name Jenkinsfile with following content

    pipeline {
    
        agent any
    
        stages {
    
            stage("build"){
                
                steps {
                    echo 'building the application'
                }
            }
    
            stage("test"){
                
                steps {
                    echo 'testing the application'
                }
            }
    
            stage("deploy"){
                
                steps {
                    echo 'deploying the application'
                }
            }
    
        }
    }

