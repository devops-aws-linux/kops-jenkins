pipeline {
    agent {
        kubernetes{
            yamlFile 'agent.yaml'
        }
    }
    stages {
        stage("GitVersion"){
            steps{
                container("maven"){
                    sh 'git --version'
                }
            }
        }
        stage("Maven Version") {
            steps {
                container("maven"){
                   sh  'mvn --version'
                }
            }
        }
        
        stage("Java Version") {
            steps {
                container("maven"){
                   sh  'java -version'
                }
            }
        }
    }
}