pipeline {
    agent {
	node {
        label  'node1'
        }
		}

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven 3.6.3"
    }

    stages {
        stage('Code Clone') {
            steps {
                git credentialsId: 'ks', url: 'https://github.com/ksrepo9/app.git'
            }
			}
		stage('mvn clean') {
            steps {
                sh 'mvn clean'      
            }
			}
		stage('mvn validate') {
            steps {
                sh 'mvn validate'      
            }
			}
		stage('mvn Compile') {
            steps {
                sh 'mvn compile'      
            }
			}
		stage('mvn Test') {
            steps {
                sh 'mvn test'      
            }
			}	
		stage('mvn Package') {
            steps {
                sh 'mvn package'      
            }
			}
				         
        }
    }
