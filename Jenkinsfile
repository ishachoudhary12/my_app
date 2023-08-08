
pipeline {
    agent any
    tools {
        maven "Maven-3.6.3"  
        jdk "JAVA"
    }
    stages {
        stage('Initialize'){
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
            }
        }
        stage('Build') {
            steps {
                dir("C:/Program Files/Jenkins") {
                sh 'make check'
                }
            }
        }
     }
    post {
       always {
           echo 'PASSED!!!'
      }
        failure {
            emailext body: 'Error ! pipeline failed', subject: 'FAILED PIPELINE', to: 'ishachoudhary521@gmail.com'
        }
   } 
}
