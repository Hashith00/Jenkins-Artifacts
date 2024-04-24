pipeline {
    agent any
 
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/Hashith00/Jenkins-Artifacts'
                
                sh 'npm install'
                
                // Run tests
                sh 'node index.js'
                
            }
        }
    }
    
    post {
        success {
            // Archive artifacts
            archiveArtifacts 'dist/**/*.js' // Example: archive compiled JavaScript files
            archiveArtifacts 'coverage/**'  // Example: archive test coverage reports
        }
    }
}