pipeline {
  agent { label "master" }
  
  stages {
    stage("build") {
      steps {
        sh """
          echo "build..."
          docker build -t hello_there .
        """
      }
    }
    
    stage("run") {
      steps {
        sh """
          echo "run..."
          docker run --rm hello_there
        """
      }
    }
  }
  
}
