pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code retrieved from GitHub'
            }
        }

        stage('Run Python Program') {
            steps {
                bat 'python --version'
                bat 'python hello.py'
            }
        }

        stage('Run Automated Tests') {
            steps {
                bat 'python -m pytest -v'
            }
        }
    }

    post {
        success {
            echo 'SUCCESS: Data Science program and tests completed!'
        }

        failure {
            echo 'FAILURE: Please check the Jenkins console output.'
        }
    }
}