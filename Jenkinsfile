pipeline {
	agent any
	
	stages {
		stage ('Compile Stage') {
			steps {
			
				withMaven(maven : 'maven_3_8_1'){
				sh '''#!/bin/bash
                  			mvn clean compile
         			'''
				 
				}
				
			}
		}
		
		
		stage ('Testing Stage') {
			steps {
			
				withMaven(maven : 'maven_3_8_1'){
				sh '''#!/bin/bash
                  	mvn test
         			'''
				}
				
			}
		}
		
		stage ('Deployment Stage') {
			steps {
			
				withMaven(maven : 'maven_3_8_1'){
				
					sh 'mvn deploy'
				 
				}
				
			}
		}
		
	}
}
