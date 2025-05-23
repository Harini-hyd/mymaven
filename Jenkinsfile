pipeline{
    agent any
    tools{
        maven 'Maven'
    }
    stages{
        stage('Checkout'){
            steps{
                git branch:'master',url:'https://github.com/Harini-hyd/mymaven.git'
            }
        }
        stage('Build'){
            steps{
                bat 'mvn clean package'
            }
        }
        stage('Test'){
            steps{
                bat 'mvn test'
            }
        }
        stage('Run Application'){
            steps{
                bat 'java -jar target/hellomaven1-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}
