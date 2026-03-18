pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building application..."
                sh 'ls -l'
            }
        }

        stage('Deploy Dev') {
            when {
                branch 'dev'
            }
            steps {
                echo "Deploying to DEV environment"
            }
        }

        stage('Deploy Test') {
            when {
                branch 'test'
            }
            steps {
                echo "Deploying to QA environment"
            }
        }

        stage('Deploy Prod') {
            when {
                branch 'main'
            }
            steps {
                echo "Deploying to PRODUCTION environment"
            }
        }
    }
}
