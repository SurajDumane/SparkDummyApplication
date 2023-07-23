pipeline {
    agent any
    tools {
        maven 'maven393'
	}
    stages {
        stage('Compile') {
            steps {
                sh 'SparkWordCount && mvn clean compile'
            }
        }
        stage('UnitTest') { 
            steps {
                sh 'SaprkWordCount && mvn clean test'
            }
        }
        stage('Package') { 
	            steps {
		         sh 'cd SparkWordCount && mvn clean package'
	     }
        }	
 
   }
}
