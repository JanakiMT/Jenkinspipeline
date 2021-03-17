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

        stage('TestLog') {
          steps {
            writeFile(file: 'logtext.txt', text: 'automation file')
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploy application'
          }
        }

        stage('Artifacts') {
          steps {
            archiveArtifacts 'logtextfile.txt'
          }
        }

      }
    }

  }
}