pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building application..."
                sh 'bash app.sh'
            }
        }

        stage('Test') {
            steps {
                echo "Running Tests..."
                sh 'echo Test Successful'
            }
        }

        stage('Archive') {
            steps {
                echo "Archiving artifacts..."
                sh 'echo Build Artifact > artifact.txt'
                archiveArtifacts artifacts: 'artifact.txt', fingerprint: true
            }
        }
    }
}
