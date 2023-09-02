pipeline {
    agent any
    stages {
        stage("Install Dependencies") {
            steps {
                sh 'bundle install'
            }
        }
        stage("Run Tests") {
            steps {
                sh 'bundle exec rspec'
            }
            post {
                success {
                    echo 'Running tests succeeded!'
                }
                failure {
                    echo 'Running tests failed!'
                }
            }
        }
    }
}
