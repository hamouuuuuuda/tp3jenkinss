pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm  // This will use the repo configured in Jenkins
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'  // For Maven projects
            }
        }

        stage('Docker Build') {
            steps {
                script {
                    docker.build("tp3-jenkins-app")
                }
            }
        }

        stage('Deploy with Docker Compose') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
