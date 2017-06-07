#!groovy

pipeline {
    agent any

    stages {
        stage ('build'){
            steps {
                sh 'exit 1'
            }
        }
    }

    post {
        always {
            // TODO This should send "Back to normal notification"
            step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                recipients: "baptiste.wicht@gmail.com",
                sendToIndividuals: true])
        }
    }
}
