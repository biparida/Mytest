// Powered by Infostretch 

timestamps {

node ('ubuntu') { 

	stage ('1stbuild - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '90206651-2f59-48f8-b20a-05d1014d2bbe', url: 'https://github.com/biparida/Mytest']]]) 
	}
	stage ('1stbuild - Build') {
 			// Shell build step
sh """ 
#!/usr/bin/env bash

echo "Hello World!" 
 """ 
	}
	stage ('My-First-Project - Build') {
 			// Shell build step
sh """ 
#!/usr/bin/env bash

echo "$BUILD_NUMBER" 
 """ 
	}
}
node ('win') { 

	stage ('2ndbuild - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '90206651-2f59-48f8-b20a-05d1014d2bbe', url: 'https://github.com/biparida/MyTest1']]]) 
	}
	stage ('2ndbuild - Build') {
 			// Batch build step
bat """ 
echo "%CHANGE_ID%"
echo "%BUILD_ID%"

dir 
 """ 
	}
}
}