pipeline {
  agent any
  stages {
    stage('Initiate') {
      steps {
        echo 'Initiating Deployment'
      }
    }

    stage('Update POC') {
      steps {
        echo 'Updating POC'
        sh 'git pull origin master'
        sh './update.py'
        sh 'sudo docker-compose build'
      }
    }

  }
}