pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Use 'checkout scm' to get the code from the repository
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // Use 'bat' instead of 'sh' for Windows
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add actual deployment steps here if needed
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
