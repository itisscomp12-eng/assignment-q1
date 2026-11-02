pipeline {
    agent any 

    stages {
        stage('Pull Code') {
            steps {
                echo 'Pulling code from GitHub...'
            }
        }
        stage('Compile Java') {
            steps {
                echo 'Compiling Hello.java...'
                sh 'javac Hello.java'
            }
        }
        stage('Execute Application') {
            steps {
                echo 'Running Hello...'
                sh 'java Hello'
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs.'
        }
    }
}

