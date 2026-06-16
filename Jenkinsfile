pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/divaforever/devops-project-1-cicd.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t germany-app:v1 .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh '''
                docker stop germany-container || true
                docker rm germany-container || true
                '''
            }
        }

        stage('Deploy Container') {
            steps {
                sh '''
                docker run -d \
                --name germany-container \
                -p 8081:80 \
                germany-app:v1
                '''
            }
        }

        stage('Verify Deployment') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
