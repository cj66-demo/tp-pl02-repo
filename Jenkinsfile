pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Etape de build"
				sh './mvnw compile' 
				
			}
		}
		stage('Tests') {
			steps { 
				echo "Etape de test"
				sh './mvnw  test' 

				
				echo "step sonar "
			}
			post {
				always {
					junit '**/target/surefire-reports/TEST-*.xml'
					}
				
			}
		}
		stage ('Deploy') {
			steps {
				 
				echo "build image docker "
				echo "push image docker to image repository"
			}
		}
	}
}
