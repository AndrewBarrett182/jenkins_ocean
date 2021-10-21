pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'hello'
        sh 'echo "sleepy time"'
        sleep 1
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'python --version'
          }
        }

        stage('test1') {
          steps {
            echo 'test'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}