pipeline {
   agent any

   tools {
      maven "maven3"
   }
   stages {
      stage('SCM') {
         steps 
		 {
            git credentialsId: 'prasad', url: 'https://github.com/Prasadagit/spring3-mvc-maven-xml-hello-world.git'
		}
	}
        stage('package') {
        steps 
        {
        sh "mvn package"
        }
    }
       stage("acrhiveArtifacts") {
           steps {
              archiveArtifacts 'target/*.war'  
           }
       }
       }
    }
