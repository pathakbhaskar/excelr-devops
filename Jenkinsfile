pipeline {
	agent any

	stages {
		stage('Install Webserver') {
			steps {
				sh 'sudo apt install apache2 -y'
			}
		}

		stage('Fetch code') {
			steps {
				git branch: 'main', url: 'https://github.com/pathakbhaskar/excelr-devops.git'
			}
		}

		stage('Deploy Application') {
			steps {
				sh 'sudo cp -R * /var/www/html/'
			}
		}

	}
}
