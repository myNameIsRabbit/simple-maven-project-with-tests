node('master') {
  checkout scm 
  stage('Build') {
    withMaven(maven: 'MAVEN_HOME') {
      'mvn install'
    }
  }
}
