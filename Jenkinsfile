pipeline {
 agent any
 stages {
  stage('Git') {
   steps {git 'https://github.com/goldcomru/sdvps-materials-popov'}
  }
  stage('Test') {
   steps {
    sh 'go test .'
   }
  }
  stage('Build') {
   steps {
    sh 'docker build . -t ubuntu-bionic:8082/hello-world:v$BUILD_NUMBER'
   }
  }
 }
}
