pipeline {
    agent any

    tools {
        maven 'Maven' // Ensure this matches the Maven tool name in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Harini-hyd/mymaven.git'
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

        stage('Run Application') {
            steps {
                sh 'java -jar target/mymaven-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}
