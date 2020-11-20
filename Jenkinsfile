pipeline {
  agent any
  stages {
    stage('scm') {
      steps {
        git(url: 'https://github.com/gowthu-dev/spring3-mvc-maven-xml-hello-world.git', branch: 'master')
      }
    }

    stage('Maven') {
      steps {
        sh 'mvn package'
      }
    }

  }
}