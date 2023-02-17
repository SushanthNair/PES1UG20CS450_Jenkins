pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS450-Pipeline PES1UG20CS450.cpp'
                build job: 'PES1UG20CS450-1'
            }
        }

        stage('Test') {
            steps {
                s './PES1UG20CS450-Pipeline'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
