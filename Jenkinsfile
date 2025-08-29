pipeline {
  agent any
  options { ansiColor('xterm') }
  stages {
    stage('Checkout') { steps { checkout scm } }
    stage('Moole Scan') {
      steps {
        mooleScan(
          credentialsId: 'sehajk',
          environment: 'ENV_005',
          onIssuesFound: 'FAIL',
          severityThreshold: 'medium',
          projectId: 'P_123'
        )
      }
    }
  }
}
