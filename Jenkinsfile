pipeline {
    agent any

    triggers {
        githubPush()  // Triggers on GitHub push via webhook
    }

    environment {
        PROJECT = "DevOpsToolkit"
    }

    stages {
        stage('Clone Repository') {
            steps {
                echo "Cloning ${PROJECT} from GitHub..."
                git 'https://github.com/GRJ-cloud/DevOpsToolkit.git'
            }
        }

        stage('Build') {
            steps {
                echo "Running a test build..."
                sh 'echo Hello from Jenkins! This is a test build for ${PROJECT}.'
            }
        }

        stage('Post-Build') {
            steps {
                echo "✅ Build completed for ${PROJECT}!"
            }
        }
    }
}
