pipeline {
  agent any
  environment{
    def msbuild = tool name: 'MSBuild', type: 'hudson.plugins.msbuild.MsBuildInstallation'
  }
  options {
    // Keep builds up to 30 days
    buildDiscarder(logRotator(daysToKeepStr: '30'))
  }

stages{
    stage ('Checkout') {
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[ CredentialsID:'fb9ec1c4-a7ab-4876-b8f9-8d13882df63d', url: 'https://alm.andritz.com/stash/scm/apt/precalc.git' ]]])
      }
    }

    stage ('Deploy') {
      steps {
          echo "Not"
      }
    }
  }
}