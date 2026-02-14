pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checkout stage from Git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage from Git'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage from Git'
            }
        }

    }

    post {

        success {
            echo 'Build Successful '
        }

        failure {
            echo 'Build Failed '
        }

    }
}
