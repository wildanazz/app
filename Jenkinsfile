pipeline {
    agent { docker { image 'node:20.15.0-alpine3.20' } }
    stages {
        stage('Build') {
            steps {
                sh 'node --version'
                sh 'echo "Building application..."'
                sh 'echo "Done."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
                sh 'echo "Done."'
            }
        }
    }
    post {
        always {
            echo 'All jobs are done.'
        }
        failure {
            mail to: 'wildanazzwa@gmail.com',
                 subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
                 body: "Something is wrong with ${env.BUILD_URL}"
        }
    }
}