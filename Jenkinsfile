pipeline{
	agent any 
	stages{
		stage("Start Grid"){
			steps{
				sh "docker-compose up -d hub chrome"
			}
		}
		stage("Run Test"){
			steps{
				sh "docker-compose up search-module book-flight-module"
			}
		}		
		stage("Bring grid Down"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}