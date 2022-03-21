node {
    
    stage ('git pull')
    {
        git branch: 'dev', url: 'https://github.com/ashumesh/Jenkins-.NET-Core-CI-CD-pipeline.git'
    }
    
    stage ('Remove')
    {
        sh 'rm -rf dot-net'
    }
	stage ('Run') {
	    sh 'nohup dotnet /var/lib/jenkins/workspace/dot-net/WebApplication/bin/Release/netcoreapp3.1/publish/WebApplication.dll --urls="http://0.0.0.0:9090" --ip="0.0.0.0" --port=9090'
	}
	
}
