pipeline {
  agent {
    label ''     // Run on a build agent where we have the Android SDK installed
  }
  options {
    // Stop the build early in case of compile or test failures
    skipStagesAfterUnstable()
  }
  stages {
     stage('Test') {
      steps {
        echo 'Testing..'
        sh './gradlew clean :core:coreTest'
      }
    }
   }
}