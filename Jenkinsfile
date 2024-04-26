pipeline {
    agent any

    stages {
       
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }


    }
    post {
        success {
            emailext 
                    body: 'Security Scan stage completed successfully.',
                    subject: 'Security Scan: Success',
                    to: 'asas385@live.com'
            }
        failure {
            emailext 
                    body: 'Security Scan stage failed.',
                    subject: 'Security Scan: Failure',
                    to: 'asas385@live.com'
        }
    }
}
                   

          

















