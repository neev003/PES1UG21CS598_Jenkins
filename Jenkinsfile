pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        script {
          // Assuming "PES1UG21CS598-1" is a Jenkins job name, you should trigger it instead of just calling build
          build "PES1UG21CS598-9"
          sh 'g++ sumn.cpp -o output'
        }
      }
    }
    stage('Test') {
      steps {
        script{
        sh './output'
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
