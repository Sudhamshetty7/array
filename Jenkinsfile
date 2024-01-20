properties([parameters([string(defaultValue: ' ', description: 'first number', name: 'a'), string(defaultValue: ' ', description: 'second number', name: 'b')])])
pipeline {
  agent {
    label 'java'
  }
  stages {
    stage('checkout') {
      steps {
        sh 'rm -rf array'
        sh 'git clone https://github.com/Sudhamshetty7/array.git'
      }
    }
    stage('run') {
      steps {
        cd /home/slave-1/workspace/array1
        sh './larnum.sh $a $b'
      }
    }
  }
}
