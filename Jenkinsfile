pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Lint') {
            steps {
                sh 'ruff check .'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }
        stage('Docker Build') {
    steps {
        sh 'docker build -t jenkins-production-cicd:1.0 .'
    }
}
stage('Health Check') {
    steps {
        sh 'curl http://localhost:5000/health'
    }
}
stage('Health Check') {
    steps {
        sh 'curl http://localhost:5000/health'
    }
}

        stage('Build') {
            steps {
                echo 'Application build completed.'
            }
        }
    }

    post {

        success {
            echo 'CI pipeline succeeded.'
        }

        failure {
            echo 'CI pipeline failed.'
        }

        always {
            echo 'Pipeline finished.'
        }
    }
}