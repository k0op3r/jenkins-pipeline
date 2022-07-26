pipeline { agent any
    
    environment { 
     PROJECT_NAME = "XOPOWO"
     OWNER_NAME   = "Max Dudko"
    }
    stages { stage('1-Build') 
           { steps { echo "Start of Stage Build" 
             echo "This project name is ${PROJECT_NAME}" 
             echo "Owner by ${OWNER_NAME}" 
             echo "Building......." 
             echo "End of Stage Build"
            }
        }
        stage('2-Test') 
           { steps { 
             echo "Start of Stage Test" 
             echo "Testing......." 
             echo "End of Stage Build"
            }
        }
        stage('3-Deploy') 
           { steps { 
             echo "Start of Stage Deploy" sh "ls -la /var/log" 
             echo "Deploying......." 
             echo "End of Stage Build"
            }
        }
        stage('4-Celebrate') 
           { steps { 
             echo "Start of Stage Celebrate" 
             echo "Yo-Ho-Ho...." 
             echo "End of Stage Build"
            }
        }
    }
}
