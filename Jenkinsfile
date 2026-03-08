pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Install Browsers') {
            steps {
                bat 'npx playwright install'
            }
        }

        stage('Run Login Test') {
            steps {
                bat 'npx playwright test tests/login.spec.js --headed --workers=2'
            }
        }

    }
}
