pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
        jdk 'jdk8'
    }
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
