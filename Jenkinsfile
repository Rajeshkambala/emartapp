pipeline {
    agent any // You can specify a specific agent label or 'any' to run on any available agent.

    stages {
        stage('Checkout') {
            steps {
                // Check out the code from the repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Replace this with your build commands
                sh 'echo "Building the project"'
            }
        }

        stage('Test') {
            steps {
                // Replace this with your test commands
                sh 'echo "Running tests"'
            }
        }

        stage('Deploy') {
            when {
                // You can add conditions to deploy only on specific branches
                expression { currentBuild.branches[0].name == 'master' }
            }
            steps {
                // Replace this with your deployment commands
                sh 'echo "Deploying the application"'
            }
        }
    }

    post {
        success {
            // Actions to perform when the pipeline succeeds
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform when the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
