pipeline {
    agent {
        docker {
            image 'maven:3.9.6-eclipse-temurin-17-alpine' 
       }
    }
    stages {
         stage('SCM') {
            steps {
                git branch: 'master',
                credentialsId: 'github-creds',
                url: 'https://github.com/CloudWithRaghu/maven-hello-devops-general.git'
           }
    }
        
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
