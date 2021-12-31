pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
              checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/abinesan1/jenkinsgit.git']]])
                          }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/abinesan1/jenkinsgit.git'
                sh 'rmdir djo'
                sh 'pwd'
                sh 'cd /var'
                sh 'mkdir djo'
                sh 'python3 test.py'
            }
        }
    }
}
