pipeline {
    agent any

    environment {
        NODEJS_HOME = tool name: 'NodeJS', type: 'NodeJS installations'
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the repository
                    git 'https://github.com/HarshitaNagar24/nodejs-app.git'
                }
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Install Node.js dependencies
                    sh 'npm install'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests (you can replace this with actual tests in your app)
                    sh 'npm test'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Build the application (e.g., if you were building assets)
                    echo 'Building application...'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy to a server (mock deployment here)
                    echo 'Deploying application...'
                }
            }
        }
    }

    post {
        success {
            echo 'The pipeline executed successfully!'
        }
        failure {
            echo 'The pipeline failed!'
        }
    }
}
