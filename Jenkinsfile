pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git '<your-repo-url>'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t yourdockerhub/jenkins-demo:v1 .'
            }
        }

        stage('Push Image') {
            steps {
                sh 'docker push yourdockerhub/jenkins-demo:v1'
            }
        }
    }
}