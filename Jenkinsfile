pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/Nithiya1227/Jenkins-kubernetes-CICD-Project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-node-app .'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }

    }
}
