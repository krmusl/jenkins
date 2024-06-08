pipeline {
  agent {
    node {
      label 'win-agent'
    }

  }
  stages {
    stage('Clean') {
      steps {
        bat 'mvn -DskipTests clean'
      }
    }

    stage('Compile') {
      steps {
        retry(count: 1)
        bat 'mvn -DskipTests compile'
      }
    }

  }
}