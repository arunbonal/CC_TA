pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'g++ hello.cpp -o hello_exec'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the project...'
                sh './hello_exec'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                // You can add actual deployment steps here
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
