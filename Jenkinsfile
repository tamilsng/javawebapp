node{
      def mvnHome = tool name: 'maven', type: 'maven' 
      stage('Checkout'){
         git 'https://github.com/tamilsng/javawebapp.git'
       
      }  
      stage('Build'){
         //// Get maven home path and build
        sh "${mvnHome}/bin/mvn clean package -Dmaven.test.skip=true"
      }
     stage ('Test-JUnit'){
         sh "'${mvnHome}/bin/mvn' test surefire-report:report"
      }   
 }
