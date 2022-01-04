pipeline {
    agent none

    stages {
        stage('Vulnerability scan') {
            environment {
                DEBRICKED_CREDENTIALS = credentials('debricked-creds')
            }

            steps {
                sh 'bash /home/entrypoint.sh debricked:scan "$DEBRICKED_CREDENTIALS_USR" "$DEBRICKED_CREDENTIALS_PSW" SCA-Debricked "$GIT_COMMIT" null cli'
            }
        }
    }
}
