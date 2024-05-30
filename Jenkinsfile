pipeline {
  agent {
    docker {
      image 'node:18.17.1-alpine3.18'
    }

  }
  stages {
    stage('Echo Build') {
      steps {
        sh 'echo Build'
      }
    }

    stage('Echo Test') {
      steps {
        sh 'sleep 5'
        sh 'echo Success!'
      }
    }

    stage('Echo Deploy') {
      steps {
        echo 'Deploy'
      }
    }

  }
}
