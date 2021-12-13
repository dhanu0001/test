pipeline {
  agent any {
  environment{
      DOCKER_TAG = getDockerTag()
  }
  stages{
      stage(build docimage){
          steps{
              sh "docker build -t dhanu001/node-app:${DOCKER_TAG}"
          }
      }  
    }
  }
}

def getDockerTag(){
    def tag = sh script: 'git rev-parse HEAD', retirnStdout: true
    return tag
}
