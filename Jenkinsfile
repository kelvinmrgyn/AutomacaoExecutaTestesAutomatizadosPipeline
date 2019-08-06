pipeline {
  agent any
  parameters{
    choice(name: 'tipo_execucao',
       choices: 'PorModulo\nCompleta\nMassaDados',
       description: 'Qual o tipo de execucao?" 
    )
  }
  stages {
    stage('Build') {
      steps {
        withMaven(maven : 'Maven'){
          sh 'mvn clean package'
        }
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
