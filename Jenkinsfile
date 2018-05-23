pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
            stage('Deploy the sharedflow') {
                steps {
                dir('edge') {
                    sh "mvn install " +
                            "    -Ptest -Denv=${params.apigee_env} -Dorg=${params.apigee_org} " +
                            "    -Dusername=${params.apigee_user} " +
                            "    -Dpassword=${params.apigee_pwd}""
                }
            }
        }
	}