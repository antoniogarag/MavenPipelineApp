pipeline{
	agent any 
	
	tools{
		maven 'Maven361'
	}

	stages{
		stage('inicio'){
			steps{
				echo 'Esto es un mensaje de inicio'
			}
		}
		stage('test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('build'){
			steps{
				sh 'mvn package'
			}
		}
		stage('Fin'){
			steps{
				echo 'El build ha finalizado'
			}
		}
		stage('Ejecucion'){
			steps{
				sh '**/target java -jar *.jar'
			}
		}
	}

}