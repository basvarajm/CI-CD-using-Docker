pipeline {
  agent any
  stages {
    stage('Test') {
    steps {
        sh "chmod +x -R ${env.WORKSPACE}"
        sh './jenkins/test.sh'
    }
}
    stage('build') {
      steps {
        echo 'Building a docker image'
        sh './scripts/build'
      }
    }
    stage('deploy') {
      steps {
        echo 'Deployment is in progress'
        sh './scripts/deploy'
      }
    }
    
  }
}
