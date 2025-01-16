## Kurzbeschreibung
Dieses Repo enthält den Deploymentprozess für das Jobscraper-Hauptprojekt (siehe <a href="https://github.com/lb-bewerbung/jobscraper-springboot">Jobscraper-Springboot</a>) in eine AWS Cloudumgebung . Es sollen nach und nach mehr Aws-Services eingebunden werden um das Hauptprojekt schrittweise in eine *Cloud-native* Architektur zu überführen.

### Aktuell eingebundene AWS-Services
1. EC2

## Servicebeschreibungen
**EC2**<br>
ec2_launch.sh verwendet das AWS CLI um 2 Instanzen zu starten. Die Sicherheitsgruppen erlauben Traffic über Http/Https und SSH.
