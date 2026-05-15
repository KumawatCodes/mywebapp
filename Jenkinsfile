pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t nginx-demo-app .'
            }
        }

        stage('Run Docker Container') {
            steps {

                bat 'docker rm -f nginx-container || true'
                bat 'docker run -d -p 8081:80 --name nginx-container nginx-demo-app'
            }
        }

    }
}   