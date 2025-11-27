pipeline{
    agent any 

    tools{

        nodejs 'Node'
    }
    stages{
        stage("Install"){
            steps{
                
                sh "npm install"
            }
           
        }

        stage("Audit"){
            steps{
                
                sh "npm audit"
                sh "npm audit fix --force"
                sh "npm outdated"
                sh "npm update"
            }
           
        }
        stage("Build"){
            steps{
                
                sh "npm run build"
            }
           
        }
        stage("Test"){
            steps{
                
                sh "npm test"
            }
           
        }
        stage("Deploy"){
            steps{
                
                echo "deploy"
            }
           
        }
    }
    post{
        
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "Ein unerwarteter Fehler ist aufgetreten"
        }
    }
}