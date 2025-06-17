
pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/YOUR-USERNAME/jenkins-docker-k8s-ci-cd.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh './scripts/build.sh'
            }
        }

        stage('Push to Docker Hub') {
            steps {
                withCredentials([string(credentialsId: 'dockerhub-token', variable: 'DOCKER_TOKEN')]) {
                    sh 'docker login -u YOUR_USERNAME -p $DOCKER_TOKEN'
                    sh 'docker push YOUR_USERNAME/your-image-name:latest'
                }
            }
        }

        stage('Deploy to K8s') {
            steps {
                sh './scripts/deploy.sh'
            }
        }
    }
}
