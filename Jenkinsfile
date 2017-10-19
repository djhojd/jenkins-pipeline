pipeline {
  agent any
  stages {
    stage('Tests') {
      parallel {
        stage('Server') {
          agent {
            docker {
              image 'maven:3-alpine'
            }
            
          }
          steps {
            sh '''echo "Building server..."
mvn --version'''
          }
        }
        stage('Client') {
          agent {
            docker {
              image 'node:6-slim'
            }
            
          }
          steps {
            echo 'Client...'
            sh '''node -v
npm -v'''
          }
        }
      }
    }
  }
}