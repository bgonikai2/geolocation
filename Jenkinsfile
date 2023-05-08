pipeline {
    triggers {
  pollSCM ('* * * * *')
    }
    agent any
    tools {
  maven 'M2_HOME'
}
    
    stages {
        stage('Maven Package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
                sleep 5
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'   
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
                
            }
        }
    }
}
