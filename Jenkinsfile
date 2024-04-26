
pipeline {
  agent any
  
  environment {
    DIRECTORY_PATH = "/Users/adhishanand/.jenkins/jobs/"
    TESTING_ENVIRONMENT = "Development"
    PRODUCTION_ENVIRONMENT = "Production"
  }
  
  stages {
    stage('Build') {
      steps {
        echo "fetch the source code from ${env.DIRECTORY_PATH}"
        echo "compile the code and generate any necessary artifacts"
      }
    }
    
    stage('Test') {
      steps {
        echo "Run unit tests"
        echo "Run integration tests"
      }
    }
    
    stage('Code Quality Check') {
      steps {
        echo "check the quality of the code"
      }
    }
    
    stage('Deploy') {
      steps {
        echo "deploying the application to ${env.TESTING_ENVIRONMENT} environment"
      }
    }
    
    stage('Approval') {
      steps {
        sleep 10
      }
    }
    
    stage('Deploy to Production') {
      steps {
        echo "Deploying the code to the ${env.PRODUCTION_ENVIRONMENT} environment"
      }
      post {
        success {
          echo "Build Successfully deployed to both environments"
        }
      }
    }
  }
}
