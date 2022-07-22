pipeline {
  agent {
    node {
      label 'slave1'
    }
  }
  tools{
    maven '3.5.4'
  }
     stages {
      stage('Removing existing directory'){
        steps {
          echo "Hello check existing directory"
          deleteDir()
        }
      }
       stage('Cloning Repo') {
        steps {
          echo "Cloning the Repo"
          sh "https://github.com/Buntyruby143/sBoot"
            }
       }
       stage('Hello Display content') {
        steps {
          echo "This is my first Multipipeline Project"
           }
       }
        stage('Building the project') {
         steps {
          dir('cBoot') {
            sh('mvn clean install')
                     }
             }
        }
        stage ('testing) {
          steps {
          dir('cBoot') {
            sh('mvn test')
                    }
             }
        }
        stage ('Deliver') {
          steps {
            dir('cBooot') {
              sh('deliver.sh')
                        }
                }
        }
    }
}
              
            
               
        
          
  
      
  
    
