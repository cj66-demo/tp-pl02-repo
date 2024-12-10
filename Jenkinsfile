pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Etape de build"
				sh './mvnw install'
				
			}
		}
		stage('Tests') {
			steps { 
				echo "Etape de test"
			}
		}
		stage ('Deploy') {
			steps {
				echo "Etape de déploiement"
			}
		}
	}
}
