pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
               
                build 'PES2UG22CS819-1'
                
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                
                sh './output'
                
            }
        }
        stage('Deploy') {
            steps {
                
                echo 'Deploying...'
            }
        }
    }
    
    post {
        failure {
           
            echo 'Pipeline failed'
           
        }
    }
}
