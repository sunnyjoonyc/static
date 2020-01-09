pipeline {
  agent any 
  stages {
    stage(‘Upload to AWS’) {
        steps {
          withAWS(region:’us-west-1’,credentials:’Jenkins’) {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’sunny-udacity-3rd-project’)
              }
            }
    }
  }
}
