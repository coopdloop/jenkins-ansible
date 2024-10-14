pipeline {
    agent any

    environment {
        GO_PATH = "/usr/local/go/bin"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh '${GO_PATH}/go build -C app -o myapp'
            }
        }

        stage('Test') {
            steps {
                sh '${GO_PATH}/go test ./...'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here
                echo 'Deploying...'
            }
        }
    }
}
