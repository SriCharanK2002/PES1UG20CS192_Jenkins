pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
            sh "make -C prog"
                echo 'Build stage completed'
            }
        }
        stage('Test') {
            steps {
                sh "/var/jenkins_home/workspace//main/hello_exec"
                echo 'Testing stage completed'
            }
        }
    }
    post {
            failure {
                echo 'Pipeline Failed'
            }
        }
}
