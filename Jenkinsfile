pipeline {
    agent any
    tools {
       maven 'MVN_3.8.6'
    }
    stages {

        stage('Maven install'){
            steps{
                script{
                    sh "mvn clean install"
                }
            }
        }

        stage('Spring Boot Start'){
            steps{
                script{
                    sh "mvn spring-boot:start"
                }
            }
        }
    }
}