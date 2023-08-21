pipeline {
  agent any
  stages {
    stage('prebuild') {
      steps {
        echo 'prebuild'
      }
    }

    stage('build') {
      steps {
        echo 'mAKE IT BUILD'
      }
    }

    stage('TEST') {
      steps {
        echo 'PLEAASE TEST IT'
      }
    }

    stage('DEPLOY') {
      steps {
        echo 'DEPLOY IT AND SEND SOME FEEDBACK'
      }
    }

    stage('REGRESSION') {
      parallel {
        stage('REGRESSION') {
          steps {
            echo 'REGRESSION '
          }
        }

        stage('CROME') {
          steps {
            echo 'CROME'
          }
        }

        stage('SAFARI') {
          steps {
            echo 'SAFARI'
          }
        }

      }
    }

    stage('FINAL DEPLOY') {
      parallel {
        stage('FINAL DEPLOY') {
          steps {
            echo 'DEV'
          }
        }

        stage('PROD DEPLOY') {
          steps {
            echo 'PROD'
          }
        }

      }
    }

  }
}