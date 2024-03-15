pipeline {
    agent any
    triggers {
        pollSCM '*/5 * * * *'
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
                echo 'npm run build'
                /* Your steps here, possibly invoking kubectl or helm */
            }
        }
    }
}