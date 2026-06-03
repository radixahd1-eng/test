pipeline {
    agent any

    stages {
        stage('Checkout (workspace)') {
            steps {
                // SCM has already checked out the repo into the workspace
                sh 'ls -la'
            }
        }
        stage('Copy into /var/jenkins_home/test') {
            steps {
                dir('/var/jenkins_home/test') {
                    git branch: 'main', url: 'https://github.com/radixahd1-eng/test.git'
                }
            }
        }
    }
}
