 
pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('Stage 1 - Check Python version') {
            steps {
                sh 'python --version'
            }
        }
      
    }
