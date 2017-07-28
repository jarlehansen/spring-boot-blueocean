#!/usr/bin/env groovy
pipeline {
    agent any
    triggers {
        cron('* * * * *')
    }

    stages {
        stage('Build') {
            steps {
                sh './gradlew build'
                archiveArtifacts artifacts: '**/build/libs/*.jar', fingerprint: true
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}