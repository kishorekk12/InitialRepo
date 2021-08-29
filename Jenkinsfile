pipeline {
  agent any
  environment {
    VERSION = '1.0'
  }
  
  stages {
    stage('code checkout') {
      steps {
        echo 'code checked out'
      }
    }

    stage('build') {
      parallel {
        stage('build') {
          when {
            expression {
              BRANCH_NAME == 'main'
            }
          }
          
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
      echo "job completed for ${VERSION}"
    }
    success{
      echo 'success'
  }
  }   
}
