pipeline {
    agent any
    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'master', 
                url: 'https://github.com/prath1234/java-hello-world-with-maven.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'Build Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}
