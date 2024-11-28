node {   
    stage('Code Clone') { 
      git credentialsId: 'ks', url: 'https://github.com/ksrepo9/app.git'
    }
    stage('Maven Clean') {
      sh 'mvn clean'      
    }
    stage('Maven Validate') {
      sh 'mvn validate'      
    }
	stage('Maven Compile') {
      sh 'mvn compile'      
    }
	stage('Maven Test') {
      sh 'mvn test'      
    }
	stage('Maven package') {
      sh 'mvn package'      
    }
}


