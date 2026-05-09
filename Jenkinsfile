pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/username/repository.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests...'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t cicd-demo .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8081:80 cicd-demo'
            }
        }
    }
}