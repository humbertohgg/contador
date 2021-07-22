pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Hello') {
      steps {
        echo "Hello beto"
      }
    }
    stage('cat README') {
      when {
        brach "fix-*"
      }
      steps {
        sh '''
          cat README.md
        '''
      }
    }
  }
}