pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Build your project using the configured Jenkins job
                build 'PES2UG22CS819-1'
                // Compile the main.cpp file
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                // Run tests on the compiled output
                sh './output'
                // Add more testing steps if necessary
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here
                echo 'Deploy...'
            }
        }
    }
    
    post {
        failure {
            // Notify failure
            echo 'Pipeline failed'
            // Add additional failure handling actions if needed
        }
    }
}
