pipeline {
	agent any
	environment {
	    PORT = credentials('PORT')
	    DATABASE_CONNECTION_STRING = credentials('DATABASE_CONNECTION_STRING')
	    CLIENT_URL = credentials('CLIENT_URL')
	    SECRET_KEY = credentials('SECRET_KEY')
	    SESSION_SECRET = credentials('SESSION_SECRET')
	    REACT_APP_SECRET_KEY = credentials('REACT_APP_SECRET_KEY')
	    REACT_APP_SITE_KEY = credentials('REACT_APP_SITE_KEY')
        }
	stages {
		//stage('Checkout SCM') {
		//	steps {
		//		git 'https://github.com/hammieee/JenkinsDependencyCheckTest.git'
		//	}
		//}

		//stage('OWASP DependencyCheck') {
		//	steps {
		//		dependencyCheck additionalArguments: '--format HTML --format XML', odcInstallation: 'Default'
		//	}
		//}
		stage('Build') {
		    steps {
			echo "Port is ${PORT}"
			echo "Client URL is ${CLIENT_URL}"
			sh 'printenv'
		    }
		}
		
	}	
	//post {
	//	success {
	//		dependencyCheckPublisher pattern: 'dependency-check-report.xml'
	//	}
	//}
}
