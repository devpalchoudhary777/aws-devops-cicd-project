pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'YOUR_GITHUB_REPO'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t devops-project .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8081:80 devops-project'
            }
        }
    }
}