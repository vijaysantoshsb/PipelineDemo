pipeline {
   agent any

   stages {
      stage('Build Apk') {
         steps {
        bat "gradlew clean"
         }
      }
   }
   post {
           always {
               emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
           }
       }
}