pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/vijai-veerapandian/simple-go-app.git' 
            }
        }

        stage('Validate Checkout') {
            steps {
                sh "ls -ltr"
            }
        }
        
        stage('Unit Tests') {
            steps {
                sh '''
                    go version
                    go test -v
                '''
            }
        }
    }
}