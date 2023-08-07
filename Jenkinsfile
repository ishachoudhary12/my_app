
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
                dir("/var/lib/jenkins/workspace/product_p/my-app") {
                sh 'make check'
                }
            }
        }
     }
    post {
       always {
           echo 'PASSED!!!'
      }
   } 
}
