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
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[ CredentialsID:'82a81d83-7f0c-42cd-9897-a5933427b37b', url: 'https://github.com/nitishNec/ansible.git' ]]])
      }
    }

    stage ('Deploy') {
      steps {
          echo "Not"
      }
    }
  }
}