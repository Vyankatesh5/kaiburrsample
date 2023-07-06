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
                script{
                    sh "pwd "
                    def image = "kaibursamplerj:${BUILD_ID}"                     
                    dockerImage = docker.build ( image, "-f Dockerfile .")

                    }
            }
        }
    }
}
