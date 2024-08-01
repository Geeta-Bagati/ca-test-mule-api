pipeline
 {
  agent any
  stages{
   stage('Build Application'){
   steps{
   bat 'mvn clean install'
   }
   }
   
   stage('Publish application to exchange'){
   steps{
   bat 'mvn deploy'
   }
   }
   
   stage('Deploy Application to cloudHub 2.0'){
   steps{
   bat 'mvn clean deploy -DmuleDeploy -X -Denv=%ENV% -DtargetName=%TARGET_NAME% -Dapp.name=%APP_NAME% -Dreplicas=%REPLICAS% -DvCores=%VCORES%'
   }
   }
  }
 } 













