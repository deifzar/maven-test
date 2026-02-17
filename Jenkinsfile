@Library('devops-pipeline-libraries') _

mavenPipeline {
  environment             = 'dev'
  repoName                = 'maven-test'
  scmProvider             = 'gitlab' // 'github' or 'gitlab'

  runTest                 = true
  runSAST                 = true // Sonarqube SAST
  runSCA                  = true
  runSBOM                 = true
  runDeployment           = true
  
  buildingImage           = 'maven:3.9.6-eclipse-temurin-17'

  scaSeverity             = 'CRITICAL,HIGH'
  trivySkipDirs           = []
  trivySkipFiles          = []
  snykSkipDirs            = []
  snykSkipFiles           = []
  createPullOrMergeRequest = true

  gitCredentialsId        = 'gitlab-pat-jenkins' // gitlab-pat-jenkins || github-app-jenkins
  snykCredentialsId       = 'snyk-pat-jenkins'
  
  sonarqubeCredentialsId  = 'sonarqube-token'  // Jenkins credentials ID for SonarQube token 
  sonarqubeUrl            = 'https://sonarqube-cptm8net.spaincentral.cloudapp.azure.com'
  sonarqubeProjectKey     = 'Maven-test' 
}