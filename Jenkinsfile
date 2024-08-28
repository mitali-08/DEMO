pipeline {
	agent any
 
	triggers {
	  pollSCM '* * * * *'
	}
	stages {
	    stage('Checkout') {
	        steps {
			git 'https://github.com/mitali-08/DEMO.git'			       
		      }}
		stage('Build') {
	           steps {
			  sh 'mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/DEMO.war /home/mitali/Documents/devops/apache-tomcat-9.0.93/webapps'
			}}	
}}
