pipeline {
  agent any

  stages {
      stage('Get code from GitHub') {
          steps {
              // Get some code from a GitHub repository
              git credentialsId: 'e90513a4-32a7-4fea-afdc-b7f16f6834d7', url: 'https://github.com/must-see/example-playbook.git'
          }
      }
      stage('Run ansible') {
          steps {
              sh 'ansible-playbook -i inventory/prod.yml site.yml'
          }
      }
  }
}
