pipeline {
	    options {
	        buildDiscarder(logRotator(numToKeepStr: '6'))
	    }
	    agent any 
	    stages {
	        stage ('maven clean'){
	            steps {
	                script {
	                    sh "mvn -f pom.xml clean"
	                }
	            }  
	        }
	        stage ('maven validate'){
	            steps {
	                script {
	                    sh "mvn -f pom.xml validate"
	                }
	            }  
	        }
	        stage ('maven compile'){
	            steps {
	                script {
	                    sh "mvn -f pom.xml compile"
	                }
	            }  
	        }
	        stage ('maven test'){
	            steps {
	                script {
	                    sh "mvn -f pom.xml test"
	                }
	            }  
	        }
	        stage ('maven package'){
	            steps {
	                script {
	                    sh "mvn -f pom.xml package"
	                }
	            }  
	        }
	        stage ('maven verify'){
	            steps {
	                script {
	                    sh "mvn -f pom.xml verify"
	                }
	            }  
	        }
	        stage ('maven install'){
	            steps {
	                script {
	                    sh "mvn -f pom.xml install"
	                }
	            }  
	        }
	        stage ('maven deploy'){
	            steps {
	                script {
	                    sh "mvn -f pom.xml deploy"
	                }
	            }  
	        }
	    }
	    post {
	    always {
	  //     archiveArtifacts artifacts: 'food-delivery-system/target/**'
	      cleanWs()
	    }
	  }
	}
