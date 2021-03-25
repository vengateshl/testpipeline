pipeline {
    agent any 
    stages {
        stage('clone repo') { 
            steps {
         
                bat "git clone https://github.com/vengateshl/testpipeline.git" 
                bat "mvn clean -f testpipeline"
            }
        }
        stage('Test') { 
            steps {
                bat "mvn test -f testpipeline"
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn package -f testpipeline"
            }
        }
    }
}
