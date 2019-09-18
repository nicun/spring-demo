  pipeline{
    agent any
    options{
    ansiColor('xterm')

  }
    stages {
    stage('git fetch'){
    steps{
    git 'https://github.com/nicun/spring-demo.git'
    }
    }
    stage('tests'){
    steps{
  bat label: '', script: 'call mvn test'
  }
  }
    stage('build'){
    steps{
  bat label: '', script: 'call mvn clean package'
  }
  }
  stage('archive'){
      steps{
    archiveArtifacts 'target/*.jar'
    echo 'oi'
    }
    }
  }
  }