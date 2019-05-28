pipeline {
  agent any
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/xpiuma/node-app'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     
    stage('Sanity Test') {
      steps {
         sh 'chmod +x script/test'
         sh 'chmod +x ./node_modules/.bin/mocha'
         sh './script/test'
      }
    }
    
    stage('Deploy to Test Env') {
      steps {
        sh 'npm -version'
      }
    }
    
    stage('Regression test suite') {
      steps {
        sh 'npm -version'
      }
    }
    
    stage('Deploy to QA Env') {
      steps {
        sh 'npm -version'
      }
    }
 stage('Deploy to Prod Env') {
      steps {
            sh 'chmod +x script/deploy'
            sh 'sudo ./script/deploy'
        }
    }
    
  }
post {
        always {
            cleanWs()
        }
    }
}
