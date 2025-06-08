pipeline{
  agent any

  tools{
    maven 'Maven'
  }

  stages{
    stage('Checkout'){
      steps{
        git branch:'master',url:'https://github.com/shar4440/maven17.git'
      }
    }

    stage('Build'){
      steps{
        sh 'mvn clean package'
      }
    }

    stage('test'){
      steps{
        sh 'mvn test'
      }
    }

    stage('run'){
      steps{
        sh 'java -jar target/maven17-1.0-SNAPSHOT.jar '
      }
    }
  }

post{
  success{
    echo 'success is finished'
  }
  failure{
    echo 'get failed'
  }
}
}
