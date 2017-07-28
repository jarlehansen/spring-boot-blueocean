#!/usr/bin/env groovy
pipeline {
    agent any
    triggers {
        cron('* * * * *')
    }

    stages {
        stage('Build') {
            steps {
                sh 'gradlew'
                archiveArtifacts artifacts: '**/build/libs/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}