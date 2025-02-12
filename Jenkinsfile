pipeline {
    agent any

    environment {
        NODEJS_VERSION = '18'
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

        stage('Test Python Scripts') {
            steps {
                sh 'python3 TyCommits/helloWorld.py'
                sh 'python3 TyCommits/sampleScript.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
}
