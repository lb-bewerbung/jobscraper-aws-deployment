## Kurzbeschreibung
Dieses Repo enthält den Deploymentprozess für das Jobscraper-Hauptprojekt (siehe <a href="https://github.com/lb-bewerbung/jobscraper-springboot">Jobscraper-Springboot</a>) in eine AWS Cloudumgebung . Es sollen nach und nach mehr Aws-Services eingebunden werden um das Hauptprojekt schrittweise in eine *Cloud-native* Architektur zu überführen.

### Aktuell eingebundene AWS-Services
1. EC2

## Servicebeschreibungen
**EC2**<br>
Das Shellscript *ec2_launch.sh* verwendet das AWS CLI um zwei Instanzen zu starten. Die Sicherheitsgruppen erlauben Traffic über Http/Https und SSH. Über den Parameter *User data* werden Commandos für das Update der Paketlisten und das Upgrade der Pakete angeordnet. Mit der aktuellen Infrastruktur sind für das Deployment nachfolgende manuelle Schritte auszuführen:

1. Instanz 1 provisionieren
   - Jenkins installieren (siehe https://github.com/lb-bewerbung/jobscraper-jenkins)
   - Ansible installieren (siehe https://github.com/lb-bewerbung/jobscraper-ansible)
   - Ansible konfigurieren
      - hosts.ini um *public Ip* von Instanz 2 ergänzen
2. Instanz 2 provisionieren und Jobscraper Webapp Deployment
   - Beim ersten Durchlauf der Jenkins Deployment Pipeline erfolgt die Provisionierung und das Deployment automatisch. 

