pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World!"'
        sh '''
          echo "Multipline shell steps work too"
          ls -lah
          '''
      }
    }
  }
}