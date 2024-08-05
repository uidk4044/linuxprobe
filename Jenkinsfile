pipeline {
    
	agent any
	options{timeout(time:150, unit: 'SECONDS')
		timestamps()
		ansiColor('xterm')
	}
	//options { disableConcurrentBuilds() }
	parameters{
		string(defaultValue: "maintainer",
		description: 'Enter user role:', name: 'userRole')
		}

	stages {
		stage('scm')
		{
			steps{
				checkout scm
			}
		}

		stage('listVals') {

			steps {
				timeout(time:80, unit: 'SECONDS'){
				checkout scm
				echo "**************************************"
				sleep 3
				echo '\033[34mHello\033[0m \033[33mcolorful\033[0m \033[35mworld!\033[0m'
				eco 'test'
				script {    def server = 'my-server-id'}
				}
			}
		}
	}
}
