pipeline {
  agent none

  stages {
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
}