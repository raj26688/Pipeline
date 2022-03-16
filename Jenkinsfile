pipeline{
	agent none
	stages {
		stage("Stage 1") {
			agent {
				label 'Group1'
			}
			steps {
				echo "welcome to melcowe"
			}
		}
		stage("Stage 2") {
			agent {
				label 'Group1'
			}
			steps {
				echo "Sleep please"
			}
		}
		stage("Hyderabad") {
			agent {
				label 'MasterGroup'
			}
			steps {
				echo "reach you soon"
			}
		}	
	}
}
