pipeline {
  agent any
  stages {
    stage('sleep') {
      parallel {
        stage('sleep') {
          steps {
            sleep 1
          }
        }

        stage('test') {
          steps {
            build(job: 'test', wait: true)
          }
        }

      }
    }

    stage('error') {
      steps {
        error 'wrong'
      }
    }

  }
}