pipeline {
    agent {
    node {
        label 'slave1'
    }
 
}
tools {
            maven '3.5.4'
}

    stages {
      stage('Delete old dir') {
            steps {
                echo 'Hello build dir'
                deleteDir()
            }
        }
        stage('clone repo') {
            steps {
                echo 'Clone repo'
                sh " git clone https://github.com/Buntyruby143/sBoot"
            }
        }
        stage('build') {
            steps {
                 dir('sBoot'){
                    sh("mvn clean install")
                 }
            }
        }
        stage('test') {
            steps {
                 dir('sBoot'){
                    sh("mvn test")
                 }
            }
        }
        stage('Build and Test completed') {
            steps {
                echo "sBoot project has been build and tested successfully"
                }
            }
        }
    }
