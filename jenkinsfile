pipeline {
    agent { label 'jenkinsslave' }

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'github-ssh-master', url: 'git@github.com:amreshsharma199/jenkins-git-integration.git'
            }
        }
        stage('Build') {
            steps {
                echo "Building the project..."
                sh 'bash build.sh'
            }
        }
        stage('Test') {
            steps {
                echo "Test stage running..."
            }
        }
    }
}
