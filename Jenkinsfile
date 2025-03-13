pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the C++ program...'
                    sh 'g++ -o output program.cpp' // Compiling the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh './output' // Executing the compiled C++ program
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'echo "Deploying application..."' // Replace with actual deploy command
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline executed successfully'
        }
    }
}
