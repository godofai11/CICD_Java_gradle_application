pipeline {
    agent {
        label 'ec2-fleet'
    }    
    stages {
        stage ("build"){
            steps{
                script{
                    docker.image('openjdk:11').inside{
                        sh 'chmod +x gradlew'
                        sh './gradlew build'
                    }    
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