pipeline {
  agent any  
  triggers { pollSCM('*/5 * * * 1-5') }
  stages {
    stage ('initial'){		
		when {
			expression {
			  return env.BRANCH_NAME.equals("master")
			}
		}
		steps {
			echo "My branch is: ${env.BRANCH_NAME}"
		}
	}
  }
}
