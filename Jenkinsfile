pipeline {
    agent {
        docker {
            image 'maven:v1' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package -Denforcer.fail=false' 
            }
        }
    }
}
