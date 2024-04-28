pipeline {
    agent any
    tools {
        nodejs 'Node'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/amankalra4/2023MT93187_Devops_Assignment'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Compile') {
            steps {
                sh 'npm run compile'
            }
        }
    }
    post {
        success {
            echo 'Build and compile successful!'
        }
        failure {
            echo 'Build or compile failed!'
        }
    }
}