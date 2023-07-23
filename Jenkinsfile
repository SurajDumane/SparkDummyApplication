pipeline {
    agent any
    tools {
        maven 'maven393'
	}
    stages {
        stage('Compile') {
            steps {
                sh 'cd SparkWordCount && mvn clean compile'
            }
        }
        stage('UnitTest') { 
            steps {
                sh 'cd SaprkWordCount && mvn clean test'
            }
        }
        stage('Package') { 
	            steps {
		         sh 'cd SparkWordCount && mvn clean package'
	     }
        }	
 
   }
}
