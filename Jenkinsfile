pipeline { 
    agent any 
    tools {
        maven 'M2_HOME'
          }
    stages {

        stage('SourceCode') {
        steps {
		git 'https://github.com/devopscbabu/maven-sample.git'
               }
            }
         stage('validate') { 
            steps { 
                sh 'mvn clean validate'
            }
        }

        stage('Build') { 
            steps { 
                sh 'mvn clean compile'
            }
        }
        stage('Package you App'){
            steps {
                sh 'mvn clean package'
            }
        }
        
    }
}
