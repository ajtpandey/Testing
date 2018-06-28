pipeline {
  agent any
  stages {
    stage('Check plan') {
      steps {
        fileExists 'Teraform.tf'
      }
    }
    stage('Confirm apply') {
      steps {
        waitUntil() {
          input 'Please say yes to execute'
        }

      }
    }
  }
}