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
                sh ' docker build -t java-maven .'
            }
        }

        stage('run docker container')
        {
            steps{
                sh ' docker run --name java-mavenC java-maven'
            }
        }

    }

}
