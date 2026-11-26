pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checkout successful!'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t krish-jenkins-demo:v1 .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8082:80 --name jenkins-pipeline-container krish-jenkins-demo:v1'
            }
        }
    }
}
