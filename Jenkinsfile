pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling the .cpp file...'
                sh 'g++ -o myProgram hello.cpp'
            }
        }

        stage('Test') {
            steps {
                echo 'Running the .cpp file...'
                sh './myProgram'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
