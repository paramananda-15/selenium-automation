pipeline {

    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/paramananda-15/selenium-automation.git'
            }
        }

        stage('Build Project') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Run Selenium Automation') {
            steps {
                sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
            }
        }

    }

}
