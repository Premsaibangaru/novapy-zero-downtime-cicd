pipeline {
agent any

options {
    timestamps()
    disableConcurrentBuilds()
}

stages {
    stage('1. Source Checkout') {
        steps {
            echo 'Checking out NovaPay source code'
            checkout scm
        }
    }

    stage('2. Build') {
        steps {
            echo 'Building the application'
            sh 'test -f README.md'
        }
    }

    stage('3. Unit Testing') {
        steps {
            echo 'Running unit tests'
            sh 'git --version'
        }
    }

    stage('4. SAST') {
        steps {
            echo 'Static application security testing stage'
            echo 'Configure SonarQube scanner when available'
        }
    }

    stage('5. Dependency and Image Scanning') {
        steps {
            echo 'Dependency and container image security scanning'
            echo 'Configure dependency scanner and Trivy'
