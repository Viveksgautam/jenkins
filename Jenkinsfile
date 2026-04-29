pipeline {
    agent any

    environment {
        CONTAINER_NAME = "nestjs-app"
        IMAGE_NAME = "nesths-image"
        EMAIL = "vivekgautam14216@gmail.com"
        PORT = "3000"
    }

    stages {
        
        stage('Build') {
            steps {
                echo 'Triggered from GitHub webhook!'
            }
        }

        stage('Send Email Notification') {
            steps {
               emailext(
                subject: "NestJS App Deployed Successfully on EC2!",
                body: "Your Nest JS app is Deployed! http://13.62.46.106:${PORT}/",
                to: "${EMAIL}"
               )
            }
        }

    }
}
