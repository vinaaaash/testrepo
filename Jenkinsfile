def pipelineToken = 'FeatureRejectedCartonsDistbff'
def jobUrl='https://lxappdevoptst01:8443/job/TDM/job/DMS/job/RLO/job/Rejected_Cartons_bff_PR/'
def qadepurl, urlToTag, depEnv, devServer, qaServer, perfServer, prodServer, deployBuildVer, nexusUrl, nexusArtifactId, nexusGroupId, artfactType, microServName, sonarQubeEnv, sonarPrjkey, sonarPrjName, sonarLgn, sonarHostUrl, depUname, depPwd, emailIds, Version, devAppHome, qaAppHome
def result = 'Starting...'
def Opt=null

def CheckoutCode(){
stage('Checkout Code') {
checkout scm
}
}
def CompileBuild(){
stage('compile and build ') {
echo "executing the compile & build method"



relDate = sh (script: "date +%m-%d-%Y", returnStdout: true).trim()
echo " value of reldate ${relDate}"
sh """npm install
pwd
ls -lrt"""



  }
}
pipeline {
  agent any
stages {
stage ('Pipeline Start'){
steps{
script{
  cleanWs()
  echo "checkout code"
  CheckoutCode()
  echo "starting compile & build"
  CompileBuild()
  }
}
}
}
}
