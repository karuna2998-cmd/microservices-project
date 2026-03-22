pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                git 'https://github.com/GoogleCloudPlatform/microservices-demo.git'
            }
        }

        stage('Build & Tag Docker Image') {
            steps {
                dir('src/adservice') {
                    sh 'docker build -t adservice .'
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'echo "Push step here (DockerHub/ECR)"'
            }
        }
    }
}
