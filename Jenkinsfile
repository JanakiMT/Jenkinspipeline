pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'building java application'
          }
        }

        stage('test') {
          steps {
            echo 'Testing the java application'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy application'
      }
    }

  }
}