pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
            stage('Deploy the sharedflow') {
                steps {
                dir('edge') {
                     bat "mvn install " +
                            "    -Pqa -Denv=${params.apigee_env} -Dorg=${params.apigee_org} " +
                            "    -Dusername=${params.apigee_user} " +
                            "    -Dpassword=${params.apigee_pwd}"
                }
            }
        }
	}
