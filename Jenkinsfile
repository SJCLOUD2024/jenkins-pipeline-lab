pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'pwd'
                sh 'touch app.txt'
                sh 'echo "App built by Jenkins - build number ${BUILD_NUMBER}" > app.txt'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application...'
                sh 'ls -la app.txt'
                echo 'Test passed: app.txt exists'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'mv app.txt deployed-app.txt'
                sh 'ls -la'
                echo 'Deployment complete'
            }
        }
    }
}
