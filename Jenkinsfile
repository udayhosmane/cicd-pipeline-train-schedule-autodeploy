pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/udayhosmane/cicd-pipeline-train-schedule-autodeploy'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run myapp npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'

            }
        }
    }
}
