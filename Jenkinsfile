@Library("react-shared-library@main") _
pipeline {
    agent any
    tools {
        nodejs 'nodejs-16.12'
    }
    stages {
        stage('Checkout') {
            steps {              
              cleanWs()
              echo "Checking out....."
              checkout scm
            }
        }  
        stage('Build App') {
            steps {
                AppBuild()
            }
        }
    }
}
