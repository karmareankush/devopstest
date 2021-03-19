pipeline {
   agent slave1
   stages{
     stage('Init'){
                    steps { echo " Testing...." }
                  }
     stage('Build'){
                    steps { echo " Building...."
                            sh 'mvn clean package '
                          }
         post {
            success {  echo "Now Archiving..."
                    archieveArtifacts artifacts: '**/target/*.jar'
                     }
               } 
     }
   }
}
