pipeline {
    agent {
        docker { image 'node:18' }
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npx jest'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}

