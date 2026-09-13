pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {

        success {
            echo 'CI/CD pipeline succeeded.'
        }

        failure {
            echo 'CI/CD pipeline failed.'
        }

        always {
            echo 'Pipeline finished.'
        }
    }
}