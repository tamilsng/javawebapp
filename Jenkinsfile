node{ 
      stage('Checkout'){
         git 'https://github.com/tamilsng/javawebapp.git'
       
      }  
      stage('Build'){
         //// Get maven home path and build
        sh "mvn clean package -Dmaven.test.skip=true"
      }
     stage ('Test-JUnit'){
         sh "mvn test surefire-report:report"
      } 
      stage ('Deploy War files'){
           sh "scp -r target/*war 13.233.133.243:/opt/docker"
      }
 }
