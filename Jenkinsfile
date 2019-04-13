node('master') {
  checkout scm 
  stage('Build') {
    withMaven(maven: 'MAVEN_HOME') {
      'mvn install'
    }
  }
  stage('Results'){
    junit '**/target/surefire-reports/TEST-*.xml'
    archive 'target/*.jar'
  }
}
