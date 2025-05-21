pipeline {
    agent any
    options {
        gitHubConnection('github-token') // Reference your credentials
    }
    stages {
        stage('Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/master']],
                    extensions: [],
                    userRemoteConfigs: [[
                        url: 'https://github.com/hamouuuuuuda/tp3jenkinss.git',
                        credentialsId: 'github-token'
                    ]]
                ])
            }
        }
        // Rest of your pipeline...
    }
}
