pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Task 15.1: Git commit triggers Jenkins build [cite: 130]
                echo 'Pulling latest code from GitHub...'
                checkout scm
            }
        }
        stage('Compile') {
            steps {
                // Task 15.2: Compile code [cite: 131]
                echo 'Compiling Java code...'
                bat 'javac Hello.java' // Use 'sh' if on Linux
            }
        }
        stage('Archive') {
            steps {
                // Task 15.3: Archive artifacts [cite: 132]
                echo 'Archiving build artifacts...'
                archiveArtifacts artifacts: 'Hello.class', fingerprint: true
            }
        }
    }
    post {
        // Task 15.4: Fail build on error 
        failure {
            echo 'CI Build Failed! Please check the code for errors.'
        }
        success {
            echo 'CI Build Successful! Artifacts are ready.'
        }
    }
}
