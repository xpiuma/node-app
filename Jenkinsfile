pipeline {
  agent {
    node {
      label 'fa'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/xpiuma/node-app'
      }
    }
    stage('') {
      steps {
        sh 'npm install'
      }
    }
  }
}