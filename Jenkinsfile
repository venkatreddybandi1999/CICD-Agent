pipeline {
    agent none
    stages {
        stage ('Backend'){
            agent {
                // docker { image 'maven:3.8.1-adoptopenjdk-11'}
                docker { image 'maven:3.8.3-openjdk-17'}
            }
            steps {
                git branch: "master", url: "https://github.com/venkatreddybandi1999/CICD-Agent.git"
                sh "mvn clean install"
            }
        }
        stage ("Deploy") {
            agent {
                docker { image 'tomcat:8.0.20-jre8'}
            }
            steps {
                echo "Tomcat image"
            }
        }
    }
}
