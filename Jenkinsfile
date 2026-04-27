pipeline {
agent any
	
	stages{
		stage('Checkout'){
			steps {
				git 'https://github.com/project/repo.git'
			
			}
		
		}
		stage('Build'){
			steps {
			sh 'mvn clean package'
			}
		}
		
		 stage('Docker Build') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
	
	}




}