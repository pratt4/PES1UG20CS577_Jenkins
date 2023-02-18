pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ working.cpp'
        build job: 'PES1UG20CS577-1'
        echo 'Built Successfully '
      }
    }
    stage('Test') {
      steps {
        sh './a.out'
        echo 'Tested Passed '
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed Successfully '
      }
    }
  }
  post{
    failure{
        echo "Pipeline failed "
    }
  }
}
