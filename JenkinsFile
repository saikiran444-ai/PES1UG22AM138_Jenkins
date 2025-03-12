pipeline{
  agent any
  stages  {
    stage("Build")  {
      steps{
        sh "g++ main.cpp -o output"
        build "PES1UG22AM183-1"
      }
    }
    stage("Test")  {
      steps{
        sh "./output"
      }
    }
    stage("Deploy")  {
      steps{
        echo "Deploy"
        sh "cat invisibleaa.cpp"
      }
    }
  }
  post  {
    failure {
      error "Pipeline failed"
    }
  }
}
