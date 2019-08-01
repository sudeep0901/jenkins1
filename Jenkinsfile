pipeline {
    agent any
     tools {
        maven 'apache-maven-3.6.0' 
    }
    stages {
        stage('Build') {
            steps {
                echo 'set'
                bat 'set'
                bat mvn --version
            }
        }
        stage("Test") {
            steps {
                echo "testing"
            }
        }
    }
    post {
        always {
            echo "Always run this "
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}