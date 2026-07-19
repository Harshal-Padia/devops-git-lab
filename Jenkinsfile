pipeline {
    agent any

    environment {
        PROJECT_NAME = "DevOps Git Lab"
    }

    stages {

        stage('Repository Info') {
            steps {
                echo "Project: ${PROJECT_NAME}"
            }
        }

        stage('Workspace') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Git Info') {
            steps {
                sh 'git branch'
                sh 'git log --oneline -5'
            }
        }

        stage('Environment') {
            steps {
                sh 'echo "Date:"'
                sh 'date'

                sh 'echo "Hostname:"'
                sh 'hostname'
            }
        }

    }

    post {

        success {
            echo 'Build Successful!'
        }

        failure {
            echo 'Build Failed!'
        }

        always {
            echo 'Pipeline Finished.'
        }

    }
}
