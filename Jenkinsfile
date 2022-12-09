pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        // kikiki03@naver.com will replace by sed command before RUN
        git url: 'kikiki03@naver.com', branch: 'main'
      }
    }
    stage('k8s deploy'){
      steps {
        kubernetesDeploy(kubeconfigId: 'kubeconfig',
                         configs: '*.yaml')
      }
    }    
  }
}