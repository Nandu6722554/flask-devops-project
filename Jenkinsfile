pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Nandu6722554/flask-devops-project'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-devops-project:v1 .'
            }
        }

        stage('Verify Image') {
            steps {
                sh 'docker images'
            }
        }
    }
}
