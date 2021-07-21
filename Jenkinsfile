pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building started..." 
                bat 'dotnet build'
                archiveArtifacts artifacts: '**/netstandard2.0/*.dll', fingerprint: true, onlyIfSuccessful: true
            }
        }
    }
}
