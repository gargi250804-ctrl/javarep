pipeline {
    agent any

    stages {
        stage('Fetch') {
            steps {
                echo 'Fetching the file'
                git 'https://github.com/gargi250804-ctrl/javarep.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building in process......'
                bat 'javac Hello.java'
            }
        }
        stage('Execute') {
            steps {
                echo 'Executing.....'
                bat 'java Hello'
            }
        }
    }
        post{
            success{
                echo 'Pipeline built successfully'
            }
            failure{
                echo 'Pipeline Failed'
            }
        }
}
