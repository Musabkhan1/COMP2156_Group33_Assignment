pipeline {
    agent any

    environment {
        NODEJS_VERSION = '18' // Use Node.js 18
    }

    tools {
        nodejs "${NODEJS_VERSION}"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Musabkhan1/COMP2156_Group33_Assignment.git'
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

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
                // Example: SCP Deployment (uncomment if needed)
                // sh 'scp -r ./dist user@your-server:/var/www/app'
            }
        }
    }
}
