pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
    }
    
  }
  stages {
    stage('Server') {
      steps {
        sh '''echo "Building server..."
mvn --version'''
      }
    }
  }
}