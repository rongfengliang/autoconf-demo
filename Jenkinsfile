pipeline {
  agent {
    node {
      label 'docker-66'
    }
    
  }
  stages {
    stage('autoconf build') {
      steps {
        sh 'autoreconf -i'
      }
    }
    stage('configure') {
      steps {
        sh './configure'
      }
    }
     stage('make') {
      steps {
        sh 'make'
      }
    }
     stage('run') {
      steps {
        sh './main'
      }
    }
  }
}
