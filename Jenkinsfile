pipeline {
    
  agent {
   
    docker {
        image 'apim-cli:latest'
        args '--entrypoint='
    }
  }
  stages {
    stage('execute') { 
        steps {
            git url: 'https://github.com/jbleroy1/devopsapim.git'
            sh '/opt/Axway/devops/scripts/apim.sh apim api  "${WORKSPACE}"/README.md'
        }
    }
  }
}
