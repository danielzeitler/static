pipeline {
  agent any
  stages {
    stage('linting') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }
    stage('Upload to AWS') {
      steps {
        withAWS(region: 'us-west-2', credentials: 'aws-static') {
          sh 'echo "Uploading to AWS..."'
            s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'dz-udacity-project')
        }
      }
    }
  }
}







