@Library('mylibrary')_

node('built-in')
{
    stage('ContDownload_Master')
    {
        cicd.newDownload("maven.git")
    }
    stage('ContBuild_Master')
    {
        cicd.newBuild()
    }
    stage('ContDeployment_Master')
    {
        cicd.newDeploy("ScriptedPipelinewithsharedlibraries","172.31.32.68","testapp")
    }
    stage('ContTesting_Master')
    {
         cicd.newDownload("FunctionalTesting.git")
         cicd.runSelenium("ScriptedPipelinewithsharedlibraries")
    }
    stage('ContDelivery_Master')
    {
        cicd.newDeploy("ScriptedPipelinewithsharedlibraries","172.31.32.210","prodapp")
    }
    
    
    
    
}
