pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'Apache Maven 3.5.2'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'Apache Maven 3.5.2'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'Apache Maven 3.5.2'){
                        bat "mvn deploy"
                }

            }
        }
    }
}
