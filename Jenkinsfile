pipeline {
    agent any

    tools {
        jdk 'JDK'
      	gradle 'gradle'
    }

    stages {

        stage('Build') {
            steps {
                sh 'gradle clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'gradle test'
            }
        }

        stage('Package') {
            steps {
                sh 'gradle package'
            }
        }
    }

    post {
        success {
            echo 'Build Successful '
        }
        failure {
            echo 'Build Failed '
        }
    }
}
