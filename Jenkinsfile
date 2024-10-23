pipeline {
  agent any

  stages {
    stage ('setup') {
      steps {
        echo 'Installation des dependances'
        sh 'pip install -r requirements.txt'
      }
    }
    
    stage ('test') {
      steps {
        echo 'Test de l_application'
        sh 'pytest tests/'
      }
    }
  }

  post {
    success{
      echo 'Success' 
    }
    failure {
      echo 'Failed'
    }
  }
}
