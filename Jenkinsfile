pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o task5 main/task5.cpp'
        sh 'nonexistent_command' // Intentional Error
        echo 'Build Successful!'
      }
    }
    stage('Test') {
      steps {
        sh 'nonexistent_command' // Intentional Error
        echo 'Test Successful!'
      }
    }
    stage('Deploy') {
      steps {
        sh 'nonexistent_command' // Intentional Error
        echo 'Successfully deployed!'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed!'
    }
  }
}
