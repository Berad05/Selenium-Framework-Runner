pipeline {
    agent any
        stages {
        stage('Create selenium Grid') {
            steps {
                bat "docker-compose -f grid.yaml up -d"
            }
        }
        stage('Run Selenium Tests') {
            steps {
                bat "docker-compose -f test-suites.yaml up"
            }
        }



    }
    post
    {
       always
       {
          bat "docker-compose -f grid.yaml down"
          bat "docker-compose -f test-suites.yaml down"

       }

    }

}