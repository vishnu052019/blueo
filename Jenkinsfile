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

    stage('Package') {
      steps {
        sh 'mvn package'
      }
    }

    stage('Deploy') {
      steps {
        sh 'java -jar target/gs-maven-0.1.0.jar'
      }
    }

    stage('End') {
      steps {
        sh 'echo "end of pipeline"'
      }
    }

  }
}