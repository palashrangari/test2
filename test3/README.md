## Jenkins Pipeline as Code.
<div id="top"></div>
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#setting-up-jenkins">Setting up Jenkins</a>
      <ul>
        <li><a href="#plugin-installation">Plugin Installation</a></li>
        <li><a href="#global-tool-configuration">Global Tool Configuration</a></li>
        <li><a href="#smtp-configuration">SMTP Configuration</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#list-of-microservices">List of Microservices</a></li>
      </ul>
    </li>
     <li>
      <a href="#pipeline-jobs">Pipeline Jobs</a>
      <ul>
        <li><a href="#build-view-jobs">Build View Jobs</a></li>
        <li><a href="#deploy-view-jobs">Deploy View Jobs</a></li>
        <li><a href="#sonar-view-jobs">Sonar View Jobs</a></li>
        <li><a href="#frontend-job">Frontend Job</a></li>
        <li><a href="#start-platform-service-job">Start Platform Service Job</a></li>
      </ul>
    </li>
  </ol>
</details>

## Setting up Jenkins

Setup Jenkins on machine with suggested plugins and install list of plugins which supports pipeline as code.

<p align="right">(<a href="#top">back to top</a>)</p>

### Plugin Installation

Plugin Installation Steps: 

   1) Install suggested plugin at the time of initial setup. 
   2) Then after setup, from dashboard, go to Manage Jenkins -> Manage Plugins -> Available. 
   3) Search for following plugins and install. 
            a) Docker API Plugin. 
            b) Docker Commons Plugin. 
            c) Docker Pipeline. 
            d) Docker Plugin. 
            e) Docker Compose Build Steps Plugin. 
            f) Docker Slaves Plugin. 
            g) docker-build-step. 

<p align="right">(<a href="#top">back to top</a>)</p>

### Global Tool Configuration  

Global Tool Configuration Steps:

   1) From dashboard, go to Manage Jenkins -> Global Tool Configuration. 
   2) Refer the images below to do configuration for Maven, JDK and Docker. 
    
   ![Maven-Configuration](https://user-images.githubusercontent.com/93180957/170216261-9a380016-9055-46aa-b0de-8787dbc3abdf.jpg)
   ![JDK-Configurations](https://user-images.githubusercontent.com/93180957/170216351-9ea7bf52-402a-4c73-8e57-cabc7ac331fb.jpg)
   ![Docker-Configuration](https://user-images.githubusercontent.com/93180957/170216393-6f961eb3-8713-406e-a6f3-e0be6506805a.jpg)
   
   3) Store Credential. Go to Manage Jenkins -> Manage Credentials. 
   
   ![Credentials-Configuration](https://user-images.githubusercontent.com/93180957/170217356-10844372-fa2c-4769-a611-a054bdbf0141.jpg)
   
   <p align="right">(<a href="#top">back to top</a>)</p>
   
### SMTP Configuration

   1) From Dashboard, Manage Jenkins -> Configure Systems. 
   2) Do the following configuration in the E-mail Notification section. 
   
   ![SMTP-Configuration](https://user-images.githubusercontent.com/93180957/170221530-745dafe9-718f-47eb-9c7a-45554d5c3164.jpeg)
    
<p align="right">(<a href="#top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

   Now after configuring Jenkins, we can start creating jobs for theesportsclub application. 

### List of Microservices

Spring Boot Microservices:

| Sr. No.  | Spring Boot Microservices  |                          GitHub URL                           |
|----------|:--------------------------:|:-------------------------------------------------------------:|
|    1     | announcement-service       | https://github.com/esportsclub/announcement-service.git       |
|    2     | banner-service             | https://github.com/esportsclub/banner-service.git             |
|    3     | game-service               | https://github.com/esportsclub/game-service.git               |
|    4     | gameid-service             | https://github.com/esportsclub/gameid-service.git             |
|    5     | image-upload-service       | https://github.com/esportsclub/image-upload-service.git       |
|    6     | invitation-service         | https://github.com/esportsclub/invitation-service.git         |
|    7     | news-service               | https://github.com/esportsclub/news-service.git               |
|    8     | reporting-service          | https://github.com/esportsclub/reporting-service.git          |
|    9     | tournament-create-service  | https://github.com/esportsclub/tournament-create-service.git  |
|    10    | tournament-get-service     | https://github.com/esportsclub/tournament-get-service.git     |
|    11    | user-create-service        | https://github.com/esportsclub/user-create-service.git        |
|    12    | user-get-service           | https://github.com/esportsclub/user-get-service.git           |
|    13    | user-preference-service    | https://github.com/esportsclub/user-preference-service.git    |
|    14    | user-Profile-service       | https://github.com/esportsclub/user-Profile-service.git       |
|    15    | mfe-host-container         | https://github.com/esportsclub/mfe-host-container.git         |

Nodejs Microservices:

| Sr. No.  |       Nodejs Microservices       |                             GitHub URL                              |
|----------|:--------------------------------:|:-------------------------------------------------------------------:|
|    1     | organisation-service-node        | https://github.com/esportsclub/organisation-service-node.git        |
|    2     | organisationmember-service-node  | https://github.com/esportsclub/organisationmember-service-node.git  |
|    3     | participant-service-node         | https://github.com/esportsclub/participant-service-node.git         |
|    4     | team-service-node                | https://github.com/esportsclub/team-service-node.git                |
|    5     | teammember-service-node          | https://github.com/esportsclub/teammember-service-node.git          |
|    6     | tournamentmember-service-node    | https://github.com/esportsclub/tournamentmember-service-node.git    |

Platform Microservices:

| Sr. No.  | Platform Microservices  |                    GitHub URL                     |
|----------|:-----------------------:|:-------------------------------------------------:|
|    1     | config                  | https://github.com/esportsclub/config.git         |
|    2     | eureka                  | https://github.com/esportsclub/eureka.git         |
|    3     | fusionauth              | https://github.com/esportsclub/infra-as-code.git  |
|    4     | ms-redis-cache          | https://github.com/esportsclub/infra-as-code.git  |
|    5     | rabbitmq-notifications  | https://github.com/esportsclub/infra-as-code.git  |
|    6     | rabbitmq-svc-comm       | https://github.com/esportsclub/infra-as-code.git  |
|    7     | zipkin                  | https://github.com/esportsclub/infra-as-code.git  |

<p align="right">(<a href="#top">back to top</a>)</p>

## Pipeline Jobs
 
Create three views in Jenkins; Build View, Deploy View, and Sonar view. Create Jenkins pipeline jobs for each microservices in each view. refer List of Microservices.
    
### Build View Jobs

Build View jobs are responsible for building the docker image for each service including frontend and Nodejs based microservices and push to the private docker registry.
    
   Let’s take an announcement-service as an example.  

   1) Go to Build View, New Item -> Enter Item Name “announcement-service-build-pl” -> select Pipeline -> click Ok. 
   2) Do the following configurations.
  
   ![announcement-service-build](https://user-images.githubusercontent.com/93180957/170230454-77c2d17c-45b0-4f79-9241-4f145cc1c459.jpeg)
   
   3) Now in Pipeline, select Pipeline Script and write a Scripted Pipeline code. The jobs in Build View will have four stages; Preparation, Package, Docker Build, Docker Push.
 
```
    node { 
    def mvnHome 
    stage('Preparation') { // for display purposes 
        // Get some code from a GitHub repository 
        git branch: 'main', 
            credentialsId: 'git-hub-access-token', 
            url: 'https://github.com/esportsclub/announcement-service.git' 
        // Get the Maven tool. 
        // ** NOTE: This 'M3' Maven tool must be configured 
        // **       in the global configuration. 
        mvnHome = tool 'M3' 
    } 
    stage('Package') { 
        // Run the maven build 
        withEnv(["MVN_HOME=$mvnHome"]) { 
            if (isUnix()) { 
                sh '"$MVN_HOME/bin/mvn" clean package -Dmaven.test.skip' 
            } else { 
                bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/) 
            } 
        } 
    } 
    stage('Docker Build') { 
        sh 'docker build -t localhost/tec/announcement-service:latest .' 
    } 
    stage('Docker Push') { 
        withDockerRegistry(credentialsId: 'docker-registry-user', url: 'https://localhost/v2') { 
            sh 'docker push localhost/tec/announcement-service:latest' 
        } 
    } 
}     
    
```
Note: For ‘Docker Push’ Stage, private registry is used to store images. 

   4) Click Save. 
   5) Click Build Now. 
   6) This is what stage view looks like after successful build.
    
   ![Stage-View-Build](https://user-images.githubusercontent.com/93180957/170233875-eb51d121-4246-4bb9-8e4a-232384268cc6.jpg)
   
   7) You can also check console output for logs.  
   8) Create pipeline jobs in Build View for all microservices in a similar fashion. 

Note: For Nodejs based microservice, skip the ‘Packaging’ Stage because these services are not a Maven project, it does not contain pom.xml. So, in Nodejs based microservice there will be three stages; Preparation, Docker Build, Docker Push. 

<p align="right">(<a href="#top">back to top</a>)</p>

### Deploy View Jobs

Let’s take an announcement-service as an example.  

   1) Go to Deploy View, New Item -> Enter Item Name “announcement-service-deploy-pl” -> select Pipeline -> click Ok. 
   2) Do the configurations as done in Build job. 
   3) Now in Pipeline, select Pipeline Script and write a Scripted Pipeline code. The jobs in Deploy View will have three stages; Preparation, Cleanup, Docker Compose. 
```
node { 
    def mvnHome 
    stage('Preparation') { // for display purposes 
        // Get some code from a GitHub repository 
        git branch: 'main', 
            credentialsId: 'git-hub-access-token', 
            url: 'https://github.com/esportsclub/announcement-service.git' 
        // Get the Maven tool. 
        // ** NOTE: This 'M3' Maven tool must be configured 
        // **       in the global configuration. 
        mvnHome = tool 'M3' 
    } 
    stage('Cleanup') { 
        sh ''' 
            docker ps -a | grep tec/announcement-service | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm  
            docker ps -a  
        ''' 
    } 
    stage('Docker Compose') { 
        sh ''' 
            docker-compose up -d --remove-orphans 
            docker ps -a | grep tec/announcement-service 
        ''' 
    } 
}      
```
   4) Click Save. 
   5) Click Build Now. 
   6) This is what stage view looks like after successful build.
   
   ![Stage-View-Deploy](https://user-images.githubusercontent.com/93180957/170237223-8041b5f8-f341-4cea-aecf-de4bdcf0b576.jpg)
   
   7) You can also check console output for logs.  
   8) Create pipeline jobs in Deploy View for all microservices in a similar fashion. 

<p align="right">(<a href="#top">back to top</a>)</p>
   
### Sonar View Jobs

Let’s take an announcement-service as an example.  

   1) Go to Deploy View, New Item -> Enter Item Name “announcement-service-sonar-pl” -> select Pipeline -> click Ok. 
   2) Do the configurations shown below. Change Poll SCM to H 8 * * *.

![announcement-service-sonar](https://user-images.githubusercontent.com/93180957/170238072-2d033d6a-26c3-45ba-a211-5ef02b2b6dfa.jpeg)

   3) Now in Pipeline, select Pipeline Script and write a Scripted Pipeline code. The jobs in Sonar View will have two stages; Preparation, Sonar. 

```
node { 
    def mvnHome 
    stage('Preparation') {// for display purposes 
        // Get some code from a GitHub repository 
        git branch: 'main', 
            credentialsId: 'git-hub-access-token', 
            url: 'https://github.com/esportsclub/announcement-service.git' 
        // Get the Maven tool. 
        // ** NOTE: This 'M3' Maven tool must be configured 
        // **       in the global configuration. 
        mvnHome = tool 'M3' 
    } 
    stage('Sonar') { 
        // Run the maven build 
        withEnv(["MVN_HOME=$mvnHome"]) { 
            if (isUnix()) { 
                sh '"$MVN_HOME/bin/mvn" clean verify sonar:sonar -Dsonar.login=45f9ed4659fa46a63467cf14056f4411c6b7709c' 
            } 
        } 
    } 
} 
```
   4) Click Save. 
   5) Click Build Now. 
   6) This is what stage view looks like after successful build. 
   
   ![Stage-View-Sonar](https://user-images.githubusercontent.com/93180957/170238821-eae44fdd-2786-40e6-9bc0-416cdcd214c4.jpg)

<p align="right">(<a href="#top">back to top</a>)</p>

### Frontend Job

Create a pipeline job for Front-end microservice. 

   1) Go to Delploy View, New Item -> Enter Item Name “mfe-host-container-deploy-pl” -> select Pipeline -> click Ok. 
   2) Do the configurations as done in Build job. 
   3) Now in Pipeline, select Pipeline Script and write a Scripted Pipeline code. 
   
```
node { 
    def mvnHome 
    stage('Preparation') { // for display purposes 
        // Get some code from a GitHub repository 
        git branch: 'main', 
            credentialsId: 'git-hub-access-token', 
            url: 'https://github.com/esportsclub/mfe-host-container.git' 
        // Get the Maven tool. 
        // ** NOTE: This 'M3' Maven tool must be configured 
        // **       in the global configuration. 
        mvnHome = tool 'M3' 
    } 
    stage('Cleanup') { 
        sh ''' 
            docker ps -a | grep tec/mfe-host-container | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm 
            docker ps -a  
        ''' 
    } 
    stage('Docker Compose') { 
        sh ''' 
            docker-compose up --build -d 
            docker ps -a | grep tec/mfe-host-container 
        ''' 
    } 
} 
```

   4) Click Save. 
   5) Click Build Now. 

<p align="right">(<a href="#top">back to top</a>)</p>

### Start Platform Service Job

Create a pipeline job that will start the platform services (config, eureka, fusionauth, ms-redis-cache, rabbitmq-notifications, rabbitmq-svc-comm, zipkin). It should first check if services are running, if yes then bring it down and restart again. For this job, no polling of SCM is required, if you want these services, just manually build the pipeline. 

   1) Go to Deploy View, New Item -> Enter Item Name “start-platform-service-deploy-pl” -> select Pipeline -> click Ok. 
   2) Do the same configurations as done in any deploy jobs. Just uncheck Poll SCM. 
   3) Now in Pipeline, select Pipeline Script and write a Scripted Pipeline code. 

```
node { 
    def mvnHome 
    stage('config') { // for display purposes 
        // Get some code from a GitHub repository 
        git branch: 'main', 
            credentialsId: 'git-hub-access-token', 
            url: 'https://github.com/esportsclub/config.git' 
        // Get the Maven tool. 
        // ** NOTE: This 'M3' Maven tool must be configured 
        // **       in the global configuration. 
        mvnHome = tool 'M3' 
        
        withEnv(["MVN_HOME=$mvnHome"]) { 
            if (isUnix()) { 
                sh '"$MVN_HOME/bin/mvn" clean package -Dmaven.test.skip' 
            } else { 
                bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/) 
            } 
        } 
         
        sh 'docker build -t localhost/tec/config:latest .' 
         
         withDockerRegistry(credentialsId: 'docker-registry-user', url: 'https://localhost/v2') { 
            sh 'docker push localhost/tec/config:latest' 
        } 
        
        withCredentials([string(credentialsId: 'palash-github-token', variable: 'GITHUBSECRET')]) { 
             sh ''' 
cat << EOF > .env 
org=tec 
image=config 
tag=latest 
port=8888 
EUREKA_SERVICE_URL=http://eureka:8761/eureka 
ZIPKIN_BASE_URL=http://zipkin:9411/ 
CONFIG_REPO=configs 
CONFIG_GIT_URI=https://github.com/esportsclub/api-config.git 
CONFIG_GIT_TOKEN=$GITHUBSECRET 
SPRING_PROFILES_ACTIVE=default 
EOF 
             ''' 
        } 
        sh ''' 
        docker ps -a | grep tec/config | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm 
        docker-compose up -d 
        docker ps -a | grep tec/config 
        ''' 
    } 
    stage('eureka') { // for display purposes 
        // Get some code from a GitHub repository 
        git branch: 'main', 
            credentialsId: 'git-hub-access-token', 
            url: 'https://github.com/esportsclub/eureka.git' 
        // Get the Maven tool. 
        // ** NOTE: This 'M3' Maven tool must be configured 
        // **       in the global configuration. 
        mvnHome = tool 'M3' 
         
        withEnv(["MVN_HOME=$mvnHome"]) { 
            if (isUnix()) { 
                sh '"$MVN_HOME/bin/mvn" clean package -Dmaven.test.skip' 
            } else { 
                bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/) 
            } 
        } 
         
        sh 'docker build -t localhost/tec/eureka:latest .' 
         
         withDockerRegistry(credentialsId: 'docker-registry-user', url: 'https://localhost/v2') { 
            sh 'docker push localhost/tec/eureka:latest' 
        } 
        sh ''' 
        docker ps -a | grep tec/eureka | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm 
        docker-compose up -d --remove-orphans 
        docker ps -a | grep tec/eureka 
        ''' 
    } 
    stage('fusionauth') { 
        git branch: 'main', 
            credentialsId: 'git-hub-access-token', 
            url: 'https://github.com/esportsclub/infra-as-code.git' 
             
        dir('fusionauth') { 
            sh ''' 
                docker ps -a | grep tec/fusionauth | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm 
                docker-compose up -d --remove-orphans 
                docker ps -a | grep tec/fusionauth 
            ''' 
        } 
    } 
    stage('ms-redis-cache') { 
        dir('ms-redis-cache') { 
            sh ''' 
                docker ps -a | grep tec/ms-redis-cache | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm 
                docker-compose up -d --remove-orphans 
                docker ps -a | grep tec/ms-redis-cache 
            ''' 
        } 
    } 
    stage('rabbitmq-notifications') { 
        dir('rabbitmq-notifications') { 
            sh ''' 
            # Create a .env file with this content for docker compose to work. 
                cat << EOF > .env 
rabbit-name-1=rabbitmq-svc-comm-1 
rabbit-name-1-port-1=5672 
rabbit-name-1-port-2=15672 
  
rabbit-name-2=rabbitmq-svc-comm-2 
rabbit-name-2-port-1=5673 
rabbit-name-2-port-2=15673 
  
rabbit-name-3=rabbitmq-svc-comm-2 
rabbit-name-3-port-1=5674 
rabbit-name-3-port-2=15674 
  
RABBITMQ_ERLANG_COOKIE=1234567890 
RABBITMQ_DEFAULT_USER=admin 
RABBITMQ_DEFAULT_PASS=admin 
EOF 
            ''' 
            sh ''' 
                docker ps -a | grep tec/rabbitmq-notifications | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm 
                docker-compose up -d --remove-orphans 
                docker ps -a | grep tec/rabbitmq-notifications 
             
            # To Join rabbit server #2 and #3 to #1 to work as a cluster 
                docker exec rabbitmq-notification-2 rabbitmqctl stop_app 
                docker exec rabbitmq-notification-2 rabbitmqctl join_cluster rabbit@rabbitmq-notification-1 
                docker exec rabbitmq-notification-2 rabbitmqctl start_app 
  
                docker exec rabbitmq-notification-3 rabbitmqctl stop_app 
                docker exec rabbitmq-notification-3 rabbitmqctl join_cluster rabbit@rabbitmq-notification-1 
                docker exec rabbitmq-notification-3 rabbitmqctl start_app 
            ''' 
        } 
    } 
    stage('rabbitmq-svc-comm') { 
        dir('rabbitmq-svc-comm') { 
            sh ''' 
                docker ps -a | grep tec/rabbitmq-svc-comm | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm 
                docker-compose up -d --remove-orphans 
                docker ps -a | grep tec/rabbitmq-svc-comm 
                 
                # Below commands to be used in case of docker container to cluster #2 and #3 with Rabbit #1. 
                # Once done it will stay clustered when started next time. 
  
                docker exec rabbitmq-svc-comm-2 rabbitmqctl stop_app  
                docker exec rabbitmq-svc-comm-2 rabbitmqctl join_cluster rabbit@rabbitmq-svc-comm-1 
                docker exec rabbitmq-svc-comm-2 rabbitmqctl start_app 
                 
                docker exec rabbitmq-svc-comm-3 rabbitmqctl stop_app 
                docker exec rabbitmq-svc-comm-3 rabbitmqctl join_cluster rabbit@rabbitmq-svc-comm-1 
                docker exec rabbitmq-svc-comm-3 rabbitmqctl start_app 
            ''' 
        } 
    } 
    stage('zipkin') { 
        dir('zipkin/zipkin-standalone') { 
            sh ''' 
                docker ps -a | grep tec/zipkin | awk '{print $1}' | xargs --no-run-if-empty docker container stop | xargs --no-run-if-empty docker container rm 
                docker-compose up -d --remove-orphans 
                docker ps -a | grep tec/zipkin 
            ''' 
        } 
    } 
} 
```

   4) Click Save. 
   5) Click Build Now.

<p align="right">(<a href="#top">back to top</a>)</p>
