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
}
}