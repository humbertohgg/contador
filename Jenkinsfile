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
        branch "fix-*"
      }
      steps {
        echo "cat README.md"
      }
    }
  }
}