pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps { echo 'Checking out code...' }
        }
        stage('Build') {
            steps { echo 'Building...' }
        }
        stage('Test') {
            steps { echo 'Testing...' }
        }
    }
    // Task 12: Post-build actions section
    post {
        success {
            echo 'SUCCESS: The build and tests finished perfectly!'
        }
        failure {
            echo 'FAILURE: Something went wrong in the pipeline.'
        }
        always {
            echo 'The pipeline execution is now complete.'
        }
    }
}
