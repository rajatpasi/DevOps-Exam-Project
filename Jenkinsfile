@'
pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                bat 'python --version'
            }
        }

        stage('Install') {
            steps {
                bat 'python -m pip install pytest'
            }
        }

        stage('Test') {
            steps {
                bat 'python -m pytest -v'
            }
        }

        stage('Build') {
            steps {
                bat 'python app.py'
            }
        }
    }
}
'@ | Set-Content -Path Jenkinsfile -Encoding ASCII