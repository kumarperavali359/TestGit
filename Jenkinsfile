pipeline {
    agent any
    options {
        checkoutToSubdirectory('source')
  }
    tools {
        maven 'M2_HOME'
        jdk 'JAVA_HOME'
 }
    stages {
        stage ('Build') {
            steps {
                dir ('source') {
                    sh '''mvn -Dmaven.test.failure.ignore=true clean install
                          cp -R target/*.war ansible/hello-world.war'''
 } }
}
}
}
}
