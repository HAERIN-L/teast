pipeline {
   agent any
   stages {
       stage('Github SourceCode Pull') {
           steps {
            
              checkout scm 
           }
       }
      stage('Docker Build') {
           steps {
            
               sh(script: 'docker-compose build app')
           }
       }
      stage('Docker Run Image') {
	        steps {
	        sh 'sudo docker run -d -p 4000:4000'
	        }
	   }
	   stage('Testing'){
	        steps {
	            echo 'Testing..'
	            }
	   }
         
   }
}
