pipeline {
    agent { 
        node {
            label 'jenkins-agent-goes-here'
            }
      }
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building nestJS application'
                sh 'npm ci'
            }
        }
        stage('Test') {
            steps {
                echo 'Running unit tests'
                sh 'npm run test'
            }
        }
        stage('Containerize') {
            steps {
                echo 'Containerizing the application'
                /* Your steps here, possibly invoking kubectl or helm */
            }
        }
    }
}