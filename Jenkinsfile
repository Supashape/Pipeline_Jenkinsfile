pipeline {
	agent any
	
	stages {
		stage ('Compile Stage') {
		
            steps{
		        withMaven(maven : 'Maven3.6.1') {
                    bat 'mvn clean compile'
                }
            }
        } 
        
        stage ('Testing Stage') {
           
            steps{
		        withMaven(maven : 'Maven3.6.1') {
                    bat 'mvn test'
                }
            }
        }

        stage ('Deployment Stage'){

            steps{
		        echo 'Deploying....'
            }
        }
    }
}
