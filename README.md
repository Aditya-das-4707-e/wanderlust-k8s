# K8S and deploy wanderlust app

1. Install Trivy
```bash
sudo apt-get install wget apt-transport-https gnupg lsb-release -y
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | sudo apt-key add -
echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list
sudo apt-get update -y
sudo apt-get install trivy -y
```
2. Setup SonarQube
```bash
docker run -itd --name SonarQube-Server -p 9000:9000 sonarqube:lts-community
```
# Steps to implement the project:
### Go to Jenkins Master and click on Manage Jenkins --> Plugins --> Available plugins install the below plugins:
1. OWASP
2. SonarQube Scanner
3. Docker
4. Pipeline: Stage View
