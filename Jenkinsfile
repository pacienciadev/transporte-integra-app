pipeline {
    agent any
    stages {
        stage('Build and install dependencies') { 
            steps {
                npm install 
            }
        }

        stage('Lint to find errors') { 
            steps {
                sh 'eslint .' 
            }
        }
        
        stage('Build App') { 
            steps {
                sh 'tsc -b && vite build' 
            }
        }
    }
}