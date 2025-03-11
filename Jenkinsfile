pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                # Compile hello.cpp and create an executable named PES1UG22AM046-1
                g++ hello.cpp -o PES1UG22AM046-1
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                # Run the compiled executable
                ./PES1UG22AM046-1
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Step Executed Successfully'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
