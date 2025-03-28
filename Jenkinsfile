pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the application using Maven/Gradle'
                }
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Running unit and integration tests using JUnit/Katalon/eggplant'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Performing code analysis using SonarQube/GitHub'
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                    echo 'Running security scan using Snyk'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Deploying application to staging server using Ansible'
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Running integration tests on staging environment using Selenium/Postman'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Deploying application to production server using Jenkins/Azure piplines'
                }
            }
        }
    }

    post {
        always {
            script {
                echo 'Sending email notification using Jenkins Email Extension Plugin...'
                mail (
                    subject: "Pipeline Notification: ${JOB_NAME} - Build #${BUILD_NUMBER}",
                    body: "The pipeline has completed. Check details at: ${BUILD_URL}",
                    to: 'akaljot4756.be23@chitkara.edu.in'
                )
            }
        }
    }
}
