pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''echo "Hello Build"
sleep 15
date'''
      }
    }

    stage('Build_Test') {
      parallel {
        stage('Build_Test') {
          steps {
            echo 'Build Test has been done'
          }
        }

        stage('Code quality test') {
          steps {
            sh '''echo "Hi QC test"
sleep 15'''
          }
        }

      }
    }

    stage('Deploy to prod') {
      steps {
        sh '''echo "you are in prod"
date
time'''
      }
    }

  }
}