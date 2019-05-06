pipeline {
    agent any
    environment {
        GIT_REPO_DIR = "${env.WORKSPACE.replace('/var/jenkins_home/', '/storage/jenkins/')}"
        NOTIFICATION_MAIL_TARGET = 'developers@tecnoclade.com.br'
        BUILD_TIMESTAMP = "${(new Date()).format("yyyy-MM-dd'T'HH:mm:ss", TimeZone.getTimeZone('UTC'))}"
    }
    stages {
        stage('Fetch') {
            steps {
                sh 'echo "$(whoami)@$(hostname):$(pwd)"'
                sh 'printenv'
            }
        }
    }
}
