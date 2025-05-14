pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Maha-9162/nodejs-app.git'  // Use your GitHub URL here
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm install'  // Install dependencies using npm
                }
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t nodejs-app .'  // Build the Docker image
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run -d -p 3000:3000 nodejs-app'  // Run the Docker container
                }
            }
        }
    }
}
