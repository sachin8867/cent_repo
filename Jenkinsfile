pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "hi"'
      }
    }
    stage('depoly') {
      parallel {
        stage('depoly') {
          steps {
            sh 'echo "job"'
          }
        }
        stage('trigger') {
          steps {
            sh 'echo "job trigger"'
          }
        }
        stage('big') {
          steps {
            sh 'echo "big"'
          }
        }
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "job1"'
          }
        }
        stage('test1') {
          steps {
            sh 'echo "add"'
          }
        }
      }
    }
  }
}
