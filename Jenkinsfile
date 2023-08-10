
pipeline {
  agent any
  
  tools {
    maven 'Maven3' 
  }

    stages {
        stage('Build Jar') {
            steps {
                echo 'Build'
              sh 'mvn clean package'
              
            }
        }

        stage('Test') {
            steps {
                echo 'Test..'
                mvn test
            }
         
        }

        stage('Deploy') {
            steps {
              echo 'Deploy'
              sh 'mvn spring-boot:run'
            }
        }
    }

}
