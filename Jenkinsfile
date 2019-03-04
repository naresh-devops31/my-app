pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                 sh "rm -rf my-app"
                 sh "git clone https://github.com/pknowledge/my-app.git/"
                 sh "mvn clean -f my-app"
                 sh "mvn compile -f my-app"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
    }
}
