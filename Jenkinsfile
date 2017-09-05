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
  post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
