pipeline {
    agent any

	options { 
		buildDiscarder(logRotator(numToKeepStr: '5'))
		timeout(time: 5, unit: 'MINUTES')
		timestamps()
	}

	triggers {
		pollSCM('* * * * *')
	}
	
    stages {
	
		stage('Check out') {
            steps {
               checkout scm
            }
        }
		
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
		
        stage('Run Unit tests') {
            steps {
                echo 'Run Unit Tests..'
            }
        }
		
		stage('Run Android Instrumentation Tests..') {
            steps {
                echo 'Run Android Instrumentation Tests..'
            }
        }
		
        stage('Code analyze') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}