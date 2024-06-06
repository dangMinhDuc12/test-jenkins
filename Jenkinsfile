@Library('groovy-test') _

pipeline {
  agent none

  stages {
    stage ('Build test') {
      agent {
        node {
            label 'ai-aws'
            customWorkspace 'home/duc/code/jenkins_agent/jenkins-test'
        }
      }

      steps {
        sh "echo helloworld"
      }
    }

    stage('Test Groovy') {
      agent {
        node {
            label 'ai-aws'
            customWorkspace 'home/duc/code/jenkins_agent/jenkins-test'
        }
      }

      steps {
        script {
          myLibraryFunctions.functionOne("Duc")
          myLibraryFunctions.functionTwo()
          myLibraryFunctions.testGetBuildCacheSize()
        }
      }
    }
  }
}