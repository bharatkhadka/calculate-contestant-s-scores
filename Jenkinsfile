node("master"){
    def mvnHome = tool name: 'mvn360', type: 'maven'
    stage("Pulling Repo"){
        echo"I'm pulling repo from Github"
        git credentialsId: 'githubaccount', url: 'https://github.com/tkkhadka/calculate-contestant-s-scores.git'

    }
    stage("Build"){
        echo "Now im building the Repo"
        sh "$mvnHome/bin/mvn clean package"
    }
}
