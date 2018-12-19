pipeline {
    agent any 
    stages {
        stage('Build docker image') { 
            steps {
                  sh "mvn -f timerlogdkr.application.parent/pom.xml clean install initialize docker:build"
            }
        }
        stage('run docker image') { 
            steps {
                sh "mvn -f timerlogdkr.application.parent/pom.xml initialize docker:start"
            }
        }
    }
}