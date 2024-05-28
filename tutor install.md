apt install apt-transport-https gpg wget curl sudo
//gpg key untuk temurin-17-jdk
wget -qO - https://packages.adoptium.net/artifactory/api/gpg/key/public | gpg --dearmor | tee /etc/apt/trusted.gpg.d/adoptium.gpg > /dev/null
apt update
apt install temurin-17-jdk
//gpg keys untuk jenkins
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee   /usr/share/keyrings/jenkins-keyring.asc > /dev/null
apt update 
apt install jenkins