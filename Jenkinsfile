pipeline {
    agent any
    tools {
        maven 'Maven' // This is the name of the Maven installation in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git credentialsId: '9c7c154b-f081-49ef-a61e-c5599ca29de8', url: 'https://github.com/farazyb/jenkins-maven-project.git'
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
        stage('Deploy') {
            steps {
                // Add your deployment steps here
            }
        }
    }
}