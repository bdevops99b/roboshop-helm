pipeline {

  agent any

  parameters {
    string(name: 'component', defaultValue: '', description: 'App Component Name')
    string(name: 'app_version', defaultValue: '', description: 'App Version')
  }

  stages {

    stage('Clone App Repo') {
      steps {
        dir('APP') {
          git branch: 'main', url: 'https://github.com/bdevops99b/${component}'
        }
        dir('HELM') {
          git branch: 'main', url: 'https://github.com/bdevops99b/roboshop-helm'
        }
      }

    }
}