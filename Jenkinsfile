 
#!/usr/bin/env groovy

pipeline {

  agent none

  options {
    buildDiscarder(logRotator(
      artifactDaysToKeepStr: '90',
      artifactNumToKeepStr: '5',
      daysToKeepStr: '180',
      numToKeepStr: '25'
    ))
    timestamps()
    skipDefaultCheckout()
  }

  stages {
    stage('stage') {
      when {
        beforeAgent true
        expression { return buildCause.isScm() }
      }
      steps {
        println "hello"
      }
    }
  }
}
