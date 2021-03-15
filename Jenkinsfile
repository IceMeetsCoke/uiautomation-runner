pipeline {
    agent any
    stages {

        stage('Start Grid') {
            steps {
                //sh
                bat "docker-compose up -d hub chrome firefox --no-color"
            }
        }

        stage('Run Test') {
            steps {
                //sh
                //no-color option will get rid of color codes showing in console log
                bat "docker-compose up bdd --no-color"
            }
        } 
    }
    post{
        always{
            archiveArtifacts artifacts: 'C:/Users/ryanchen/WorkSpaces/LogixPanel/test-result/**'
            //sh
            bat "docker-compose down --no-color"
        }
    }
}