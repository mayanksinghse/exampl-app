node {
     def app
     stage ('Clone Repository'){
         checkout scm
   }
   stage ('build image')
   {
     app=docker.build('mayanksinghse/mayank')
  }
  stage ('push image')
  {
     docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credential'){
              app.push('latest')
	}
  }

}
