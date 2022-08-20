pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh '''pwd
whoami
date
ls'''
      }
    }

    stage('Build1') {
      parallel {
        stage('Build1') {
          steps {
            echo 'Hey This is first build'
          }
        }

        stage('Build2') {
          steps {
            echo 'Hey This is second build'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Web Server is exposed to the world'
        sleep 10
      }
    }

  }
}