// 1. Basic pipeline using docker python image, to show its version and running python file.  

/**
pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('Stage 1 - Check Python version') {
            steps {
                sh 'python --version'
            }
        }
        stage('Stage 2 - Run hello world') {
            steps {
                sh 'python src/hello_world.py'
            }
        }
    }
}
**/

/** 2. When the Pipeline has finished executing, you may need to run clean-up steps or perform some actions based on the outcome of the Pipeline. 
These actions can be performed in the post section. **/

pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'echo "Fail!"; exit 1'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
