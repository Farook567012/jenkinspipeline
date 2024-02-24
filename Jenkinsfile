pipeline {
  agent any
  stages {
    stage('plan') {
      steps {
        echo 'paln for pipeline'
      }
    }

    stage('Code') {
      steps {
        echo 'Prepare code'
      }
    }

    stage('Build') {
      steps {
        echo 'Build code for pipeline'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test code'
          }
        }

        stage('Release') {
          steps {
            echo 'Release code'
          }
        }

        stage('Deploy') {
          steps {
            echo 'Deploy to production'
          }
        }

        stage('operate') {
          steps {
            echo 'Operate code'
          }
        }

      }
    }

  }
}