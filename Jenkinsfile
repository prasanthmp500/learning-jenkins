pipeline {
    agent { docker { image 'maven:3.3.3' } }
 
   stages {

        stage('version') {
            steps {
                sh 'mvn --version'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

    }


}