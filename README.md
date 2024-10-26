# samplehub-ctf

le site fait appelle à un fichier json (sample.json) qui chargé dans le body

il est chargé par un js coté client 
<img width="1345" alt="Screenshot 2024-10-26 at 21 42 02" src="https://github.com/user-attachments/assets/af7f2f46-372d-45c6-b383-af161e7957d0">


si l'on intercepte dans burp on peut voir la première requête du site web
<img width="567" alt="Screenshot 2024-10-26 at 21 35 56" src="https://github.com/user-attachments/assets/8e389bdc-a8ad-46e5-9b29-d701e320951a">

Une fois que la requête est passé le js est éxecuté et récupère le fichier sample.json ce qui nous donne la 2eme requête
<img width="567" alt="Screenshot 2024-10-26 at 21 36 17" src="https://github.com/user-attachments/assets/bd693f07-a5ae-4a8b-9e31-d62f96fa7577">

si l'on modifie la réponse de la deuxième requête comme ceci:
<img width="846" alt="Screenshot 2024-10-26 at 21 37 25" src="https://github.com/user-attachments/assets/6a3db042-fc08-4be8-bbac-8000660407ed">

voici la page qui m'a aider a comprendre ou était la vuln 
<img width="1408" alt="Screenshot 2024-10-26 at 21 47 39" src="https://github.com/user-attachments/assets/8bc15cfc-7d6f-4d72-be18-a365cda0f2a3">

On peut balancer notre payload et forward la requête 
<img width="1021" alt="Screenshot 2024-10-26 at 21 38 02" src="https://github.com/user-attachments/assets/cd30fa91-f6c9-403c-8a4d-5e07a0fb0301">

voici la page une fois chargé (afficher tout les fichier en mettant "." dans la barre de recherche
<img width="1405" alt="Screenshot 2024-10-26 at 21 38 57" src="https://github.com/user-attachments/assets/8eab76e1-9e5d-4181-aa97-77d6e85ebfa1">

si l'on regarde burp on voit notre payload qui était interprété
<img width="516" alt="Screenshot 2024-10-26 at 21 39 12" src="https://github.com/user-attachments/assets/e3cc488d-365f-41b8-a34a-fefe8802b00f">

on peut donc forward la requete et revenir sur la page pour constater
<img width="1337" alt="Screenshot 2024-10-26 at 21 39 28" src="https://github.com/user-attachments/assets/885b8d1e-14e8-404e-a40e-ea94866ce00b">
