pipeline {
    agent any

    stages {

        stage('Repository Information') {
            steps {
                echo 'Repository cloned successfully!'
            }
        }

        stage('Workspace') {
            steps {
                sh 'pwd'
            }
        }

        stage('List Files') {
            steps {
                sh 'ls -la'
            }
        }

        stage('Read README') {
            steps {
                sh 'cat README.md'
            }
        }

        stage('Git Information') {
            steps {
                sh 'git branch'
                sh 'git log --oneline -3'
            }
        }

    }

    post {

        always {
            echo 'Cleaning up...'
        }

        success {
            echo 'Pipeline executed successfully!'
        }

        failure {
            echo 'Pipeline failed.'
        }

    }
}
