pipeline {
    agent any

    tools {
        nodejs 'Node'
    }

    stages {
        stage('Build and install dependencies') { 
            steps {
                bat 'npm install' 
            }
        }

        stage('Lint to find errors') { 
            steps {
                bat 'eslint .' 
            }
        }
        
        stage('Build App') { 
            steps {
                bat 'tsc -b && vite build' 
            }
        }
    }
}