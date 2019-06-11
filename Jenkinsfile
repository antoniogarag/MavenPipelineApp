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
				sh 'mvn package -Dmaven.test.skip=true'
			}
		}
		stage('Fin'){
			steps{
				echo 'El build ha finalizado'
			}
		}
		stage('Ejecucion'){
			steps{
				sh 'java ´jar *.jar > kkk.out'
				def out = readFile 'kkk.out'
			}
		}
	}

}