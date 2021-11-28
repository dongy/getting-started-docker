pipeline {
  agent { label "master" }
  
  stages {
    stage("build") {
      steps {
        sh """
          cd docker
          docker build -t hello_there .
        """
      }
    }
    
    stage("run") {
      steps {
        sh """
          docker run --rm hello_there
        """
      }
    }
  }
  
}
