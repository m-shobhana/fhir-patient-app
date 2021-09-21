pipeline 

{ 

   agent any 

   stages{ 

     stage('Build Application'){ 

     steps{ 

     bat 'mvn clean install' 

     } 

     } 

     stage('Deploy Application to Mulesoft CloudHub'){ 

     steps{ 

     bat 'mvn package deploy -DmuleDeploy'  

     } 

    } 

     stage('Perfrom Regression Testing'){ 

     steps{ 

     bat 'C:\\Users\\SHOBHM\\AppData\\Roaming\\npm\\newman run C:\Users\SHOBHM\Postman_collection\Patient.postman_collection.json
     } 

    } 

    stage('SonarQube Testing'){ 

    steps{ 

    bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=f4c18d4d00473a2ebb7dcd38844a79c8b868fd75' 

    } 

   } 

     

  } 

} 