pipeline {
	agent any
	options {
	withAWS(region:'us-east-2', credentials:'aws-static',profile:'myProfile')
}
	stages {
		stage('Upload to AWS'){
			steps{
				sh 'echo "Hello World"'
				sh'''
					echo "Multiline shell steps works too"
					ls -lah
				'''
				s3Upload(file:'index.html', bucket:'project3test', path:'/home/ubuntu/index.html')
			}
		}
	}
}