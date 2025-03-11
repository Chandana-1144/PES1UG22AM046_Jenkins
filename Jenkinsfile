pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello'
            }
        }
        stage('Test') {
            steps {
                sh './hello'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Step Executed'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
