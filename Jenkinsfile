pipeline{
    agent any
    stages {
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
