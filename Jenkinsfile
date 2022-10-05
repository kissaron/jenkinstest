pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                 bat "mvn -Dmaven.test.failure.ignore=true  clean compile"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                  bat "mvn -Dmaven.test.failure.ignore=true test "
            }
        }
        stage('Deploy') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true  install"
            }
        }
    }
}
