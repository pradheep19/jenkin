pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Pulling latest code from GitHub...'
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling Java code...'
                bat 'javac Hello.java'
            }
        }

        stage('Archive Artifacts') {
            steps {
                echo 'Archiving .class file...'
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }

    }

    post {

        success {
            echo 'CI Pipeline Successful '
        }

        failure {
            echo 'CI Pipeline Failed '
        }

    }
}
