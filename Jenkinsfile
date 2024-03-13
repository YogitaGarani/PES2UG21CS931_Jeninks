pipeline {
  agent any
  stages {
    stage('Build') {
      steps 
        build 'PES2UG21CS931-1'
        sh 'g++ main/hello.cpp -o output'
      }
    } 
    stage('Test') {
      steps {
          sh './output'
      }
    }
    stage('Deploy') {
      steps {
          echo'deploy'
      }
    }
  }
  post {
    failure {
        error 'Pipeline Failed'
    }
  }
}
