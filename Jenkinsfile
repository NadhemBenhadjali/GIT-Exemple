pipeline {
    agent any
    tools {
        jdk 'JDK21'
    }
    stages {
        stage('Checkout code') {
            steps {
                git branch: 'master', url: 'https://github.com/NadhemBenhadjali/GIT-Exemple'
            }
        }
        stage('Compile code') {
            steps {
                sh 'mkdir -p build'
                sh 'javac -d build src/application/Test.java'
            }
        }
        stage('Execute code') {
            steps {
                sh 'java -cp build application.Test'
            }
        }
        stage('display message') {
            steps {
                echo 'Hello from github'
            }
        }
    }
}
