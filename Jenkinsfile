pipeline {
  agent any

  stages {
    stage('Checkout') {
        steps {
           Get some code from a GitHub repository
          git branch 'main', url 'https://github.com/kristina-abrahamyan/lbg-vat-calculator.git'
        }
    }
    stage('SonarQube Analysis') {
      environment {
        scannerHome = tool 'sonarqube'
      }
        steps {
            withSonarQubeEnv('sonar-qube-1') {        
              sh ${scannerHome}binsonar-scanner
            }   
        }
    }
  }
}