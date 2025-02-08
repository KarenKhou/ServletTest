##Devoir 2: Details 
##Etape 1:
Telecharger Tomcat 10 Apache Tomcat® - Apache Tomcat 10 Software Downloads Core zip file
Extraire le fichier zip dans le fichier C:\Tomcat
##Etape 2 : CMD
cd C:\Tomcat\bin
C:\Tomcat\bin>startup.bat Pour active tomcat
##Etape 3: Tester Tomcat 
http://localhost:8080 

##Etape 4: Sur Inellij Ultimate
Setting : Ajoute le web server apache :
 
Cliquer sur + et ajouter le path de tomcat. 
##Etape 5 : Créer un Projet jakarta EE
##Etape 6 : Le code Implementation du servlet 
Compilation : javac -cp "C:\Tomcat\lib\servlet-api.jar" -d out/production/monProjet src/BonjourServlet.java

##Etape 7 : Deployer sur tomcat
Tomcat recherche les servlets dans WEB-INF/classes/
Alors pour deployer il faut :
✅ Créer le dossier C:\Tomcat\webapps/monProjet/WEB-INF/classes/ 
✅ Copier BonjourServlet.class dans WEB-INF/classes/ 
✅ Relancer Tomcat et tester

 
Attention il faut que mon jdk et mon tomcat version soit compatible.
Pour ce devoir j ai utiliser les version :
java version "18.0.2.1" 2022-08-18
Server version: Apache Tomcat/9.0.98
##Etape 8 : Créez une page html qui contient un lien vers le Servlet
On cree index.html :
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Test Servlet</title>
</head>
<body>
<h1>Bienvenue</h1>
<a href="http://localhost:8080/DevoirServlet/bonjour">Accéder au Servlet</a>
</body>
</html>
 puis on deploie dans C:\Tomcat\webapps\DevoirServlet 


 
quand je clique sur le lien mon servlet se lance.
