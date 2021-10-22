node{
	def maven = tool name: "maven363"
	stage("Checkout"){
		git 'git@github.com:leenajob/myProjectjava.git'
	}
	stage("Build"){
	  sh'mvn clean compile'	
}
	stage("Test"){
	sh 'mvn test'
	junit '**/target/surefile-report/TEST-*.xml'
	}
	stage("Package"){
	    sh 'mvn package'
	}		
}	

