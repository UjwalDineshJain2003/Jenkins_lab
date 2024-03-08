pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS684-1'
                sh 'g++ hello.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline Failed'
        }
    }
}
