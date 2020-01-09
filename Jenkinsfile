pipeline {
  agent any 
  stages {
    stage(‘Upload to AWS’) {
        steps {
          withAWS(region:’us-west-1’, credentials:’jenkins’) {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’sunny-udacity-3rd-project’)
              }
            }
    }
  }
}
