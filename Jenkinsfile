environment {
    registry = "poojansds/webapp:v1"
    dockerImage = ""
  }

  agent any

  stages {

    stage('Cloning our Git') {
      steps {
       echo 'cloning'
        git 'https://github.com/NarayanPooja/jenkintest'
      }
    }

    stage('Build image') {
      steps{
         echo 'Building image..'
        script {
          dockerImage = docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }

    stage('Deploy') {
      steps{
        script {
          docker.withRegistry( "", registryCredential ) {
            dockerImage.push()
          }
        }
      }
    }
      }
    }

  }

}
