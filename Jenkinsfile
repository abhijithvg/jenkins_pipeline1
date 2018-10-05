pipeline {
  agent {
    node {
      label 'node1'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh '''echo "Testing..."
echo "Testing1..."'''
            sh 'sleep 10'
          }
        }
        stage('Test2') {
          steps {
            sh 'echo "TestingA..."'
            sh 'sleep 20'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
      }
    }
  }
}