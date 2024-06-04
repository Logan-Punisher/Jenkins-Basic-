pipeline {
    agent {
        docker { image 'node:16-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'npm -v'
            }
        }
        
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'node app.js'  // Corrected the file name here
            }
        }
    }
}
