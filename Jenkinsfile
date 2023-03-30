pipeline {
    agent any
    tools {
       maven 'MVN_3.8.6'
       jdk 'Java17'
    }
    stages {
        stage('Which Java?') {
            steps {
                sh 'java --version'
            }
        }

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

        stage('Curl'){
            steps{
                script{
                    sh "curl localhost:8081"
                }
            }
        }
    }
}
