node {
     def app
     stage ('Clone Repository'){
         chheckout scm
   }
   stage ('build image')
   {
     app=docker.build('mayank/exampl-app')
  }
  stage ('push image')
  {
     docker.withRegistery('https://registry.hub.docker.com','docker-hub-credential'){
              app.push('latest')
	}
  }

}
