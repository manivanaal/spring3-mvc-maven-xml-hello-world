pipeline {
    agent any
     tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven 3"
    }
    stages {
        stage("clone gitrepo") {
        steps {
           git credentialsId: 'github_cred', url: 'https://github.com/manivanaal/spring3-mvc-maven-xml-hello-world.git'
        }
      }
      stage("execute maven") {
        steps {
           sh "mvn package"
        }
      }
   }
}
