pipeline {
    agent any

    environment {
        IMAGE_NAME = "hello-world-docker"
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/<your-repo>.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t $IMAGE_NAME .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run --rm $IMAGE_NAME'
                }
            }
        }
    }
}
