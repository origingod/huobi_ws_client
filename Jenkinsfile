pipeline {
  agent {
    docker {
      image 'ubuntu'
      args '16.04'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            echo 'hello'
            
          },
          "cat processlist": {
            sleep '1'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Chrome": {
            echo 'testing in chrome'
            
          },
          "Firefox": {
            echo 'testing in firefox'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploying'
      }
    }
  }
}