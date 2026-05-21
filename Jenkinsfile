pipeline{
    agent any
    stages{
        stage('build maven app')
        {
            steps{
                sh 'mvn clean package'
            }
        }

        stage('build docker image')
        {
            steps{
                sh 'sudo docker build -t java-maven .'
            }
        }

        stage('run docker container')
        {
            steps{
                sh 'sudo docker run --name java-mavenC java-maven'
            }
        }

    }

}
