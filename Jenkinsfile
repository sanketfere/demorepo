pipeline {
    agent any

    stages {
     
        stage('Fetch') {
            steps {
                echo 'Fetching from Repo...'
                git 'https://github.com/sanketfere/demorepo.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building from program...'
                bat 'javac dummy.java'
            }
        }
         stage('Execute') {
            steps {
                echo 'Executing...'
                bat 'java dummy'
            }
        }
    }
    post{
        success{
            echo 'pipeline built successfully'
        }
        failure{
            echo 'pipeline failed'
        }
    }
}
