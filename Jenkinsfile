pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                sh 'sudo docker build -t abalone .' 
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'sudo docker run -p 8000:8000 -d abalone'
            }
        }
    }   
}
