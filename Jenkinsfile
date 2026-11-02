pipeline {
    agent any 

    stages {
        stage('Pull Code') {
            steps {
                // Code is automatically pulled if configured via 'Pipeline from SCM'
                echo 'Pulling code from GitHub...'
            }
        }
        stage('Compile Java') {
            steps {
                echo 'Compiling HelloWorld.java...'
                sh 'javac Hello.java'
            }
        }
        stage('Execute Application') {
            steps {
                echo 'Running HelloWorld...'
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
