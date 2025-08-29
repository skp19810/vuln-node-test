pipeline {
  agent any
  options { ansiColor('xterm') }
  stages {
    stage('Checkout') { steps { checkout scm } }
    stage('Moole Scan') {
      steps {
        mooleScan(
          credentialsId: 'abcd',
          environment: 'ENV_005',
          onIssuesFound: 'FAIL',
          severityThreshold: 'medium',
          projectName: 'P_123'
        )
      }
    }
  }
}
