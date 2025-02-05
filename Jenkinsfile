pipeline {
    agent any

    environment {
        // Retrieve the SonarCloud token from Jenkins credentials
        SONAR_TOKEN = credentials('sonarcloud-token')
    }

    stages {
        stage('Checkout') {
            steps {
                // Check out your project from GitHub
                git url: 'https://github.com/anushka129/CurrencyConverter.git'
            }
        }
        stage('Build') {
            steps {
                // If you have build steps (e.g., if you use npm scripts), run them here.
                // For a simple HTML/CSS/JS project, you might skip this.
                echo 'Building the project...'
            }
        }
        stage('Test') {
            steps {
                // If you have any tests (e.g., JavaScript tests with a framework), run them here.
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                // For a static site, you could deploy to GitHub Pages, AWS S3, or another hosting service.
                echo 'Deploying the project...'
            }
        }
    }
    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
