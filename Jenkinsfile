pipeline{
	agent any
tools{
	maven 'Maven'
	}
stages{
	stage('Checkout'){
		steps{
			git branch:'master',url:'https://github.com/Shukruth-Gowda/gu1.git'
			}
		}
	stage('Build'){
		steps{
			sh'mvn clean package'
		}
	}
	stage('Test'){
		steps{
			sh'mvn test'
		}
	}
	stage('Run Application'){
		steps{
			sh'java -jar target/Mymavenguva-1.0-SNAPSHOT.jar'
		}
	}
}
post{
	success{
		echo 'Build and deployment success'
		}
	failure{
		echo 'Build failure'
		}
	}
}
