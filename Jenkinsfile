node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
      // Get maven home path
      // def mvnHome =  tool name: 'maven-3', type: 'maven'
      def mvnHome =  tool name: 'Maven3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
  stage('Email Notification'){
      mail bcc: '', body: '''Hello shiva,

         This is a test mail. Welcome to Jenkins pipeline''', cc: 'siva.gummaji@gmail.com', from: 'anil.akj72@gmail.com', 
         replyTo: '', subject: 'Jenkins Test Job', to: 'siva.aug07@gmail.com'
   }     
   
   // Here I commented this slack notification.
   
  /*   stage('Slack Notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/',
       channel: '#jenkins-pipeline-demo',
       color: 'good', 
       message: 'Welcome to Jenkins, Slack!', 
       teamDomain: 'javahomecloud',
       tokenCredentialId: 'slack-demo'
    }    */  
}
