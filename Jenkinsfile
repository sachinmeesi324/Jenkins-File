@Library("shared-libs1") _

pipeline {
    agent any

    stages {  
         stage('Maven Build') {
            steps {
               sh 'mvn clean package'
            }
        }
        
        stage("TomCat Deploy") {
            steps {
                 tomcatDeploy("172.31.37.72","ec2-user","tomcatdev","Jenkins-File.war")
            }
        }
    }
}
