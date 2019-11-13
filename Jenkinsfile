node{
def mvnHome
stage('Preparation'){
	git 'https://github.com/beereshwebapp/Java1.git'
	mvnHome = tool 'maven-3.6.2'
}

stage('Build'){
	withEnv(["MVN_HOME=$mvnHome"]){
	  bat(/"%MVN_HOME%/bin/mvn" clean compile install/)
	}
}
stage('Test'){
	echo 'Testing completed'
}
}