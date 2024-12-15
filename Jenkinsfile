pipeline {
    agent any
        stages {
        stage('Run Test cases') {
            steps {
                bat "docker-compose up"
            }
        }
        stage('Delete Container') {
            steps {
                bat "docker-compose down"
            }
        }



    }

}