pipeline {
  agent any
  stages {
    stage('Clean') {
      steps {
        sh 'sleep 1'
      }
    }
    stage('Checkout') {
      steps {
        sh 'sleep 1'
      }
    }
    stage('Builds') {
      steps {
        parallel(
          "Build core": {
            sh 'sleep 1'
            
          },
          "Build component": {
            sh 'sleep 2'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        waitUntil() {
          sleep 1
        }
        
      }
    }
    stage('Deploy') {
      steps {
        sleep 1
      }
    }
  }
}
