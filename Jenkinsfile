pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test step'
          }
        }

        stage('Test parallel') {
          steps {
            echo 'Parllel'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
        sleep 10
      }
    }

  }
}