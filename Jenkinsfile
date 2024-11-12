pipeline {
    agent any
//
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'apache-maven-3.9.2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'apache-maven-3.9.2') {
                    sh 'mvn test'
                }
            }
        }

//
        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.9.2') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
