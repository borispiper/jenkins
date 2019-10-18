pipeline {
    agent {
        docker {
            image 'node:12.4-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
        USERNAME = credentials('USERNAME')
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
                stage('Deploy') {
            steps {
                sh ''
            }
        }
    }
}
