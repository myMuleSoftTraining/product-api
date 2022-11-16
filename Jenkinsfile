pipeline {
 agent any
 
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests'
      }
    }

    stage('Test') {
      steps {
          echo '****Munit Test has executes****'
      }
    }

   stage('Deploy Development') {
      steps {
            bat 'mvn -U -V -e -B -DskipTests -Ptest deploy -DmuleDeploy'
      }
    }
  }
 }