pipeline {
    agent {
        docker {
            image 'openjdk:11'     // Use official OpenJDK Docker image
            args '-v $PWD:/app -w /app' // Mount current dir and set working dir (optional but helpful)
        }
    }

    stages {
        stage('Verify Java Version') {
            steps {
                sh 'java -version'
            }
        }

        stage('Compile Java') {
            steps {
                sh 'javac Helloworld.java'
            }
        }

        stage('Run Java Program') {
            steps {
                sh 'java HelloWorld'
            }
        }
    }
}
