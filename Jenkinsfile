pipeline{
    agent any
    tools{
    	gradle 'gradle'
    	jdk 'java-11'
    }
    stages{
    	stage('checkout'){
    	   steps{
    	      git branch:'master', url:'https://github.com/Darshan2610/ggd.git'
    	   }
    	   
    	}
        stage('build'){
            steps{sh 'gradle build'}
        }
        stage('running'){
            steps{sh 'gradle run'}
        }
    }
    
    post{
    success{echo 'sucess'}
    failure{echo 'failed'}
    }
}
