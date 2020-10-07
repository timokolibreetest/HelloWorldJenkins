 
pipeline {

  agent none

  options {
    buildDiscarder(logRotator(
      artifactDaysToKeepStr: '90',
      artifactNumToKeepStr: '5',
      daysToKeepStr: '180',
      numToKeepStr: '25'
    ))
    skipDefaultCheckout()
  }

  stages {
    stage('stage') {
      steps {
        println "hello not skiped"
                scmSkip(deleteBuild: true, skipPattern:'skipci')

      }
    }
  }
}
