pipeline {
    agent any
    stages {
	
		stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'dev',
                credentialsId: '085f3680-f68a-4665-a8f8-b7dced60dd05',
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
