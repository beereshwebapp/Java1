node{
def mvnHome
stage("Preparation"){
	git 'https://github.com/beereshwebapp/Java1.git'
	mvnHome = Tool 'maven-3.6.2'
}

stage("Build"){
	WithEnv(["MVN_HOME=$mvnHome"]){
	  bat "%MVN_HOME%/bin/mvn clean compile install"
	}
}
}