pipeline {
    
	agent any

    }
	
    environment {
        NEXUS_VERSION = "nexus3"
        NEXUS_PROTOCOL = "http"
        NEXUS_URL = "10.10.1.4:8081"
        NEXUS_REPOSITORY = "Applogin-release"
	NEXUS_REPOGRP_ID    = "applogin-group"
        NEXUS_CREDENTIAL_ID = "nexuslogin"
        ARTVERSION = "${env.BUILD_ID}"
    }
	
        stage('CODE ANALYSIS with SONARQUBE') {
          
		  environment {
             scannerHome = tool 'sonarqube 4.7'
          }


   stages {
   
     stage('Install Dependencies') { 
        steps { 
           sh 'npm install' 
        }
     }
     
     stage('Test') { 
        steps { 
           sh 'echo "testing application..."'
        }
      }

         stage("Deploy application") { 
         steps { 
           sh 'echo "deploying application..."'
         }

     }
  
   	}

   }
