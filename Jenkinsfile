pipeline {
    agent any
    tools {
        maven 'maven' // This is the name of the Maven installation in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git  url: 'https://github.com/farazyb/jenkins-maven-project.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}