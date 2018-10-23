pipeline{
  agent any
  stages {
    stage('Clean Workspace'){
      steps{
        cleanWs()
      }
    }
    stage('Build'){
      steps{
        echo 'Building..'
        sh './gradle build'
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
      }
    }
    stage('Test'){
      steps{
        echo 'Testing..'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deploying..'
      }
    }
  }
}
