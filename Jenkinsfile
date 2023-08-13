pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Build your code here
            }
        }
        stage('Test') {
            steps {
                // Test your code here
            }
        }
        stage('Manual Approval') {
            steps {
                input message: 'Lanjutkan ke tahap Deploy?', submitter: 'user', parameters: [
                    [$class: 'BooleanParameterDefinition', defaultValue: true, description: '', name: 'proceed']
                ]
            }
        }
        stage('Deploy') {
            when {
                expression { params.proceed == true }
            }
            steps {
                // Deploy your code here
            }
        }
    }
}
