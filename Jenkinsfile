pipeline {							
    agent any							
    parameters {							
        string(name: 'environment', defaultValue: 'Dev', description: 'Environment to build for (Valid values: Dev, Test, Prod)')
		string(name: 'version', defaultValue: '1.0', description: 'Version number to build for')
		booleanParam(name: 'to_deploy_to_environment', defaultValue: true, description: '')
		choice(choices: 'US-EAST-1\nUS-WEST-2', description: 'What AWS region?', name: 'region')
		text(name:'myText', defaultValue:'myTextValue', description:'myText')
		password(name:'myPassword', defaultValue:'myPasswordValue', description:'myDescription')
		file(name:'myFile', description:'fileDescription')
		credentials(name:'myCredentials', description:'myCredentailsDesc', required:true)					
    }							
    stages {							
        stage('Example') {							
            steps {							
                echo "We are building for ${params.environment}, ${params.version}, and we are deploying to environment: ${params.to_deploy_to_environment}"
				echo "region:${params.region}, myText: ${params.myText}, myPassword: ${params.myPassword}, and myFile: ${params.myFile}"
				echo "selected credentials is: ${params.myCredentials}"
            }							
        }							
    }							
}					
