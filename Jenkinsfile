pipeline {
  agent any
  stages {
    stage('code checkout') {
      steps {
        echo 'code checked out'
      }
    }

    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'compilaton'
          }
        }

        stage('test') {
          steps {
            echo 'test checked out code'
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
  post{
    always{
    }
    success{
      echo 'success'
  }
    
}
