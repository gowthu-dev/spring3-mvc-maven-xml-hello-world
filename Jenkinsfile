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

    stage('deploy') {
      steps {
        sh 'sh "curl -v -u tomcat-credentials -T /var/lib/jenkins/workspace/Blueocean_spring_master/target/spring3-mvc-maven-xml-hello-world-1.3.war \'http://ec2-18-188-149-36.us-east-2.compute.amazonaws.com:8989/manager/text/deploy?path=/Blueocean-spring-pipeline&update=true\'"'
      }
    }

  }
}