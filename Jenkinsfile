pipeline	{
	agent	{
		label 'MasterGroup'
	}
	triggers {
		pollSCM '* * * * *'
	}
	stages	{
		stage ("clone GOL - Githib Central Repo") {
			steps	{
				git 'https://github.com/wakaleo/game-of-life.git'
			}
		}
		stage ("Build GOL - MAVEN") {
			steps	{
				sh 'mvn clean package'
			}
		}
		stage ("Archive articrafts") {
			steps	{
				archiveArtifacts artifacts: 'gameoflife-web/target/*war', followSymlinks: false
			}
		}
		stage ("Junit Test Reports") {
			steps	{
				junit 'gameoflife-web/target/surefire-reports/*.xml'
			}
		}
	}	
}
