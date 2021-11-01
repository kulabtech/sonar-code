pipeline {
 agent any
 tools{
     maven 'Maven'
      }
     stages{
         stage('CheckoutCode')
          {
            steps
             {
                git credentialsId: 'git_creds', url: 'https://github.com/kulabtech/sonar-code.git' , branch: 'sonarqube-8'
             }
          }
         stage ('Build') 
         {
            steps 
            {
                sh 'chmod +x gradlew'
                sh './gradlew clean build
            }
        }            
    }
}
