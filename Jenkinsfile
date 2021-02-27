pipeline {
  agent { label 'linux' }
  tools {
    maven 'maven363'
  }
  stages {
    stage('checkout7') {
      steps {
        git 'https://github.com/pavandata/myProject.git'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
        junit '**/target/surefire-reports/TEST-*.xml'
      }
    }
    stage('Package') {
      steps {
        sh 'mvn package'
      }
    }
  }
}
