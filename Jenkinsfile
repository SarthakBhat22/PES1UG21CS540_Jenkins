pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling the .cpp file...'
                sh "g++ -o test test.cpp"
            }
        }

        stage('Test') {
            steps {
                echo 'Running the .cpp file...'
                sh "./nonexistent-executable"
            }
        }

        stage('Build PES1UG21CS540-1 Project') {
            steps {
                echo 'Triggering PES1UG21CS540-1 project build...'
                build job: 'PES1UG21CS540-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the program...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
