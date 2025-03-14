pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS135-1'
                sh 'cd main && g++ -o main_cs135 main.cpp'
                echo 'Build success'
            }
        }
        stage('Test') {
            steps {
                sh './main_cs135'
                echo 'Test success'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployed successfully'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
