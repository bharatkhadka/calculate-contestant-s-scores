node("agent"){
    def mvnHome = tool name: 'mvn360', type: 'maven'
    stage("Getting Repo"){
        echo "I'm getting repo"
        git credentialsId: 'githubaccount', url: 'https://github.com/bharatkhadka/calculate-contestant-s-scores.git'
        
    }
    
    stage("Clean Test"){
        echo "I'm doing clean test"
        sh "$mvnHome/bin/mvn clean test"
        
    }
    
    stage("Build"){
        echo "Now i'm building"
        sh "$mvnHome/bin/mvn clean package"
    }
    
}
