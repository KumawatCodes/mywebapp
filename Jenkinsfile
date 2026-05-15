pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t mywebapp'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker rm -f mypage-container||true'
                bat 'docker run -d -p 8181:80 --name mypage-container mywebapp'
            }
        }

    }
}   