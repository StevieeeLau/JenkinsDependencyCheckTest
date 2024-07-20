pipeline{
	agentany
	stages{
		stage('CheckoutSCM'){
			steps{
				git 'https://github.com/nlct2k/JenkinsDependencyCheckTest.git'
			}
		}
 
		stage('OWASPDependency-CheckVulnerabilities'){
			steps{
				dependencyCheckadditionalArguments: '''-o'./'-s'./'-f 'ALL'--prettyPrint''',odcInstallation: 'OWASPDependency-CheckVulnerabilities'
				dependencyCheckPublisherpattern: 'dependency-check-report.xml'
			}
		}
	}
}
