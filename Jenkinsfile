pipeline{
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'mvn test'
            } post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Build/Test'){
            steps {
                sh "mvn clean package"
            }
        }
        stage('Deploy'){
            steps {
                sh "java -jar spring-penguins-0.0.1-SNAPSHOT.jar"
            }
        }
    }
}
