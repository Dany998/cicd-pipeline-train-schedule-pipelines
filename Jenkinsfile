pipeline {
 
  agent any
  
  stages {
    
    stage("build") {
      
       steps {
           echo 'Building the application.......'
           sh './gradlew build --no-daemon' 
       }
      
    }
    
  }
  
  post {
     always {
         archiveArtifacts artifacts: 'dist/trainSchedule.zip' 
     }
  }
  
}
