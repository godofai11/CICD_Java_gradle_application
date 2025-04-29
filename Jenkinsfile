pipeline {
    agent any
    stages {
        stage ("build"){
            agent {
                docker {
                    image 'openjdk:11'
                }            
            }
            steps{
                script{
                    sh 'chmod +x gradlew'
                    sh './gradlew build'
                }
            }
        }

        stage("docker build "){
            steps{
                script{
                    sh 'docker ps'
                }
            }
        }            
    }
}    