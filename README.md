# Session
Project session html seulement JEE
Atelier 3: Gestion des Sessions
Les Servlets et les sessions
 Développer une application web JavaEE, constituée de :

Une page html index , permettant la saisie de l’identifiant de l’user voulant se connecter sur le site. ce formulaire appelle  la servlet ControlAcces.  
Cette servlet contrôle l’accès au   site en vérifiant si l’identifiant saisi figure parmi les identifiants valides mémorisés dans un tableau hashTable usersAuthorized <String, String> déclaré comme attribut privé dans la servlet et qui sera chargé dans la méthode init() par les identités associés aux noms des utilisateurs autorisés à y accéder. En cas d'une authentification correcte l'user sera dirigé vers une deuxième servlet AccesSite affichant le nom associé de l’user connecté et la structure du site sous la forme d’un menu. la première servlet communiquera le nom de l’user connecté via un paramètre de session. Dans le cas échéant il sera redirigé de nouveau vers la page index.html pour s'authentifié de nouveau.
La page affichée par la deuxième servlet contiendra un lien de déconnexion exécutant une servlet pour la déconnexion.    La servlet de déconnexion détruit la session et libère la mémoire, et renvoie l'user vers la page index.  

response.sendRedirect(servlet) , HttpSession session= request.getSession();

session.setAttribute("name", vnom).

String vlog= (String) session.getAttribute("name");
