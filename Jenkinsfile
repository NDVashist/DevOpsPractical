pipeline {
    agent any
    tools {
        maven 'M1'
    }
    stages {
        stage('fetch') {
            steps {
                echo 'Fetching the Maven Project from github'
                git branch: 'main',
                url: 'https://github.com/NDVashist/DevOpsPractical.git'
            }
        }
        stage('validate') {
            steps {
                echo 'Validating the Maven Project'
                bat 'mvn validate'
            }
        }
        stage('clean') {
            steps {
                echo 'Cleaning the Maven Project'
                bat 'mvn clean'
            }
        }
        stage('compile') {
            steps {
                echo 'Compiling the Maven Project'
                bat 'mvn compile'
            }
        }
        stage('test') {
            steps {
                echo 'Testing the Maven Project'
                bat 'mvn test'
            }
        }
        stage('package') {
            steps {
                echo 'Packaging the Maven Project'
                bat 'mvn package'
            }
        }
        stage('verify') {
            steps {
                echo 'Verifying the Maven Project'
                bat 'mvn verify'
            }
        }
        stage('install') {
            steps {
                echo 'Installing the Maven Project'
                bat 'mvn install'
            }
        }
        stage('executing generate jar') {
            steps {
                echo 'Executing the generate jar file'
                bat 'java -jar ./target/Sum.jar 10 25 30 55 67 89'
            }
        }
    }
}
