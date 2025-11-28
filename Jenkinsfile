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