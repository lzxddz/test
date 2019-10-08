pipeline {
    agent any
    stages {
        /* "Build" and "Test" stages omitted */

        stage('Deploy - Staging') {
            steps {
                sh 'mvn --version'
                sh 'echo $JAVA_HOME'
            }
        }

        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }

        stage('Deploy - Production') {
            steps {
                sh 'echo "run deploy"'
            }
        }
    }
}