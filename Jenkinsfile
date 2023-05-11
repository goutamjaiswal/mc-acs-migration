pipeline {
	agent any
	stages {
		stage("Sample"){
		steps {
			echo "Hello"
			}
		}
		stage("Ingress Creation"){
			steps{
				mkdir mc-csf-deploy && cd mc-csf-deploy
				git credentialsId: 'github-token', url: 'https://github.com/acquia/mc-csf-deploy.git'
				sh '''
					cd aws-migration
					ls
				 '''
			}
		}
	}
}
