pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o program program.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './program'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
