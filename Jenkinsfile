pipeline{
    agent any
    stages{
        stage("GIT checkout"){
            steps{
                git credentialsId: 'samson', url: 'git@github.com:samsonappu/sample-java.git'
            }
        }
        stage('Maven Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'  
            }
        }
        stage('Maven Test') {
            steps {
                sh 'mvn test'   
            }
        }
    }
}
