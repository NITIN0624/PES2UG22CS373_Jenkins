pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS373-1'
                sh 'g++ main.cpp -o output'
                sh 'make -C main'
            }
        }
        stage('Test') {
            steps {
                sh './main/hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
