pipeline {
  agent any
  stages {
    stage('code') {
      steps {
        git(url: 'https://github.com/vishnu052019/simple_maven.git', poll: true, changelog: true)
      }
    }

    stage('Compile') {
      steps {
        sh 'mvn compile'
      }
    }

  }
}