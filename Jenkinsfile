pipeline {
    agent any
    stages {
	
		stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'dev',
                credentialsId: '6ddc111d-f89e-475a-a431-51a8693de3ae',
                url: 'https://github.com/markondareddy/Jenkins-pipeline-maven.git'

                  }          
        }
	
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven') {
                    bat 'mvn clean compile'
                }
            }
        }
       stage ('Testing Stage') {

          steps {
             withMaven(maven : 'Maven') {
              //bat 'mvn test'
              }
            }
        }
       stage ('Install Stage') {
           steps {
               withMaven(maven : 'Maven') {
                   // bat 'mvn install'
               }
            }
       }
    }
}
