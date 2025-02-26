pipeline {
  agent any 
  tools {
    maven 'Maven'
  }
  environment {
        JAVA_HOME = "/usr/lib/jvm/java-11-openjdk-amd64"
  }
  stages {
    stage ('Initialize') {
      steps {
        sh '''
            echo "PATH = ${PATH}"
            echo "M2_HOME = ${M2_HOME}"
        ''' 
      }
    }
    stage('Build') {
      steps { 
        sh 'mvn clean package'
      }
    }
  }
}
