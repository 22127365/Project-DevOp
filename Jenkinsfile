pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/22127365/Project-DevOp.git'
      }
    }
    stage('Build Docker Image') {
      steps {
        script {
          docker.build('my-app')
        }
      }
    }
    stage('Run Docker Containner') {
      steps {
        script {
          docker.run('my-app', '-p 3000:3000')
        }
    }
  }
}
