pipeline{
  agent any

  stages{
    stage('Build Docker image from Docker file'){
      steps{
        script{
          bat "docker build -t xacuti01/dock."
        }
      }
    }
    stage('build and run docker container'){
      steps{
        script{
          bat "docker rm -f proj9 || exit0"
          bat "docker run -d --name proj9 xacuti01/dock"
        }
      }
    }
  }
}
