pipeline {
  agent any
  stages {
    stage('Deploy - Mobfs') {
      steps {
        sh 'docker ps -f name=${containerName} -q | xargs --no-run-if-empty docker stop'
      }
    }
    stage('Test - Mobsf') {
      steps {
        sh 'chmod 755 test/runUAT.sh'
      }
    }
  }
}