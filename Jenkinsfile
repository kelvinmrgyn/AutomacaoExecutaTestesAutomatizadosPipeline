pipeline {
  agent any
  parameters {
    gitParameter (branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH')
    choice(name: 'tipo_execucao',
       choices: 'PorModulo\nCompleta\nMassaDados',
       description: 'Qual o tipo de execucao?')
  }
  stages {
    stage('Build') {
            steps {
				git branch: "${params.BRANCH}", url: 'http://kelvin.rocha:K3lvin@004@ferramentasgo.centralit.com.br:8080/scm/git/citsmart-itsm-enterprise'
			}
		}
    stage('Test') {
      steps {
        sh 'make'
      }
    }
    stage('Deploy') {
      steps {
        sh 'make'
      }
    }
  }
}
