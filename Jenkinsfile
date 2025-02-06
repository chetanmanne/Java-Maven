pipeline {
    agent any
    tools{
        maven 'maven-3.9.9'
    }
    stages{
        stage('Build Maven'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/chetanmanne/Java-Maven']]])
                sh 'mvn clean install'
            }
        }
    }
}
