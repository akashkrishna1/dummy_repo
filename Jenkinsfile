pipeline {
    agent any
    // tools {nodejs "NODEJS"}
stages {
  stage('Checkout') {
       steps {
            script {
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/akkrish11/dummy_repo.git']]])
 }
 }
}
stage('SonarQube analysis') {

      steps {

        script {

          // requires SonarQube Scanner 2.8+

            SCANNER_HOME = tool 'sonarqube'

        }

        withSonarQubeEnv('SonarQube') {

          bat "$SCANNER_HOME/bin/sonar-scanner -Dsonar.projectKey=demo -Dsonar.sources=. -Dsonar.login=squ_d6f7abe55883817c2b4a63efd01fe65c806b7d0f"

        }

      }

    }
}
}