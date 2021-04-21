pipeline {
    agent any
    stages {

        // stage('Start Grid') {
        //     steps {
        //         //sh
        //         bat "docker-compose up -d hub chrome firefox"
        //     }
        // }

        stage('Run Test') {
            steps {
                //sh
                //no-color option will get rid of color codes showing in console log
                // bat "docker-compose up bdd"
                bat "docker compose up"
            }
        } 
    }
    post{
        always{
            // archiveArtifacts artifacts: 'target/*.html'
            //sh
            bat "docker-compose down"
        }
    }
}