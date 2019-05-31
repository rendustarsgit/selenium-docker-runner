pipeline{
	agent any 
	stages{
		stage("Start Grid"){
			steps{
				sh "docker-compose up -d hub chrome firefox--no-color"
			}
		}
		stage("Run Test"){
			steps{
				sh "docker-compose up search-module book-flight-module --no-color"
			}
		}		
		stage("Bring grid Down"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}