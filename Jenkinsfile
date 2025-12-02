pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
                echo "Source code checked out"
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-demo .'
            }
        }

        stage('Run Image') {
            steps {
                sh 'docker run --rm jenkins-demo'
            }
        }
    }
}
