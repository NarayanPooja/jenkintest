pipeline {
  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/NarayanPooja/jenkintest.git'
      }
    }

    stage('Build image') {
      steps{
        script {
          echo "Building"
        }
      }
    }

    stage('Push Image') {
      steps{
        script {
          echo "Pushing"
        }
      }
    }

    stage('Deploy App') {
      steps {
        script {
          echo "Deploying"
        }
      }
    }

  }

}
