pipeline { 
    agent any 
    stages {
           stage('Checkout') {
              steps {
                  git url: ‘https://github.com/aknam/SpringBoot.git’
           }
         }
        stage('Build') { 
            steps {
                withMaven(maven : 'MAVEN 3.6'){
                        sh "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'MAVEN 3.6'){
                        sh "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'MAVEN 3.6'){
                        sh "mvn deploy"
                }

            }
        }
    }
}
