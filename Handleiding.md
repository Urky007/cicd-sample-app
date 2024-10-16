# Handleiding Labo 1
## Handige commando's
- sudo docker ps -a
 - Geeft de huidige bestaande docker containers weer en handige info zoals : Container ID, Image, status,...
- Sudo docker start *Container ID*
 - Start de container op
- Sudo docker stop *Container ID*
  - Stopt de container
- Sudo Docker rm *Container ID*
  - Verwijderd de container

## Extra informatie
Jenkins is een applicatie die ervoor zorgt dat updates automatisch kunnen doorgevoerd worden. De manier hoe dit werkt is:
- Start de Jenkins container op de vm
- Ga naar de jenkins webpagina (In dit geval http://192.168.56.20:8080/)
- Start een bouwpoging bij de pipeline die je wilt starten.
  - deze verwijst naar een jenkinsfile die opgeslagen is in het git project
- Controleer dat alles succesvol is verlopen (In dit geval surf naar http://192.168.56.20:5050/). 
  
## Problemen
Een probleem die ik ondervond bij het maken van dit labo was dat ik een error kreeg bij het **opnieuw** runnen van de sample_app build. De oplossing die ik hiervoor gebruikte was:
- Aanpassing in sample_app.sh
  - Toevoegen van controles op het bestaan van de mappen: tempdir, tempdir/templates en tempdir/static