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
                sh 'sudo docker build -t abalone' .
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'sudo docker run -p 9000:9000 -d abalone'
            }
        }
    }   
}
