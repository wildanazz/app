pipeline {
    agent { docker { image 'node:20.15.0-alpine3.20' } }
    stages {
        stage('Build') {
            steps {
                sh 'node --version'
                sh 'echo "Building application..."'
                sh 'echo "Build done."'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing application..."'
                sh 'echo "Test done."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
                sh 'echo "Deploy done."'
            }
        }
    }
    post {
        success {
            echo 'All jobs are done.'
        }
    }
}