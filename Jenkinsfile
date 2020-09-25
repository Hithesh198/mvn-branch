@Library('shared-library2') _
pipeline{
    agent any
    stages{
	  stage('Git Checkout SCM') {
            steps{
               
                gitcheckout(
                    branch: "master",
                    url: "https://github.com/shreyadonthula/mvn-branch.git"
                )
            }
        } 
	    
         stage("build"){
            steps{
                script{
                    build()
                }
            }   
        } 
       stage("Test"){
            steps{
                script{
                    test()
                }
            }   
        }
	 stage("Package"){
            steps{
                script{
                    packaging()
                }
            }   
        }
		
	
	 stage("Stages"){
            steps{
               
                echo "last stage"
             }
        }
    }   
}
