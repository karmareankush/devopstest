pipeline {
   agent { label 'slave1' }
   stages{
     stage('Init'){
                    steps { echo " Testing...." 
                            sh 'ifconfig -a'                 
                          }
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
