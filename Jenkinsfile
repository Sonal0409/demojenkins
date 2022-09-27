pipeline{
    
    tools{
        jdk 'myjava'
        maven 'mymaven'
    }
    
    agent none
    
    stages{
        
        stage ('Parallel execution')
        {
        parallel{
            
        stage('Clone a repo')
        {
            agent any
            steps{
            git 'https://github.com/Sonal0409/DevOpsCodeDemo.git' 
            }
        }
         stage('package the code')
        {
            agent { label 'linux_slave'}
            steps{
            git 'https://github.com/Sonal0409/DevOpsCodeDemo.git' 
            sh 'mvn package'
            
            }
        }
        }
        
        }
    }
    
    
}
