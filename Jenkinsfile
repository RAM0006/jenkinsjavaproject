pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/RAM0006/jenkinsjavaproject.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar'
            }
        }
    }
}
