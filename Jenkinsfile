pipeline {
    agent any
	stages {
		stage('Checkout and Run First Script') {
			steps {
				script {
					// Запускаем скрипты
					echo 'Running test1.sh in a separate shell'
					sh 'chmod +x test1.sh' 
					sh 'nohup ./test1.sh &' 
				}
			}
		}
			
		stage('Checkout and Run Second Script') {
	            steps {
	                script {
	                	echo 'Running test2.sh in steps'
	                	sh 'chmod +x test2.sh' 
	                	sh './test2.sh' 
				}
			}
		}
			
		stage('Checkout and Run Third Script') {
	            steps {
	                script {
	                	echo 'Running test3.sh'
	                	sh 'chmod +x test3.sh' 
	                	sh './test3.sh' 
	            		}
			}
		}
	}	
}