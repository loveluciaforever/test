pipeline {
  agent any
  stages {
    stage('check out') {
      parallel {
        stage('check out') {
          steps {
            echo 'check out code from git'
          }
        }

        stage('build') {
          steps {
            echo 'build code'
            bat(returnStatus: true, returnStdout: true, script: 'test.bat')
          }
        }

        stage('check result') {
          steps {
            echo 'check the build result and notifer someone'
          }
        }

        stage('deploy') {
          steps {
            echo 'deploy the build fruits on web and shared folder'
          }
        }

      }
    }

  }
}