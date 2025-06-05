pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build with Maven') {
      steps {
        sh 'mvn clean install'
      }
    }
  }

  post {
    success {
      echo '✅ Build and dependency resolution succeeded!'
    }
    failure {
      echo '❌ Build failed – check Maven output'
    }
  }
} 
