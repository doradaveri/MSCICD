pipeline {
    agent any
    environment
    {
        PATH = '/Applications/apache-maven-3.6.2/bin:$PATH'
    }
    stages 
    {
        stage('Git Checkout') 
        {
            steps 
            {
                echo 'Code'
                git 'https://github.com/doradaveri/MSCICD'
            }
        }
        
        stage('Maven Build') 
        {
            steps 
            {
                echo 'Build'
                sh 'mvn clean package'
            }
        }
    }
    
    post { 
        always 
        { 
            echo 'End'
        }
    }
}
