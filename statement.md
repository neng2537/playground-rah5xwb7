# Débutter en PHP !

    *   Script d'initiation à PHP
	* 	Auteur: MERY Ludovic
	*
	*	Pour toi Public de SIO 1  !!!
	*
	*	Penser à avoir votre serveur web apache démarré qui écoute sur le port 80
	*	Penser à avoir votre Serveur MySQL démarré qui écoute localement (127.0.0.1) sur le port 3306
	*	Placer ce fichier dans un dossier correspondant à votre projet (mkdir debutterphp)
	*	Placer ce dossier dans le repertoire de publication d'apache (C:\wamp\www) pour ceux qui bossent sous wamp.
	*	Créer la base de données "debutterphp" ou avec un autre nom mais adapter votre code sous MySQL (perso j'utilise phpmyadmin mais vous pouvez faire autrement)
	*	Créer la table "profs" (ou un autre nom mais il faudra adapter le code notamment la requete SQL)
	*	Insérez y des données.
	*	Tester votre code avec un navigateur en faisant http://127.0.0.1/debutterphp
	*	La gestion des noms de domaine de type www.monsite.fr peut se faire si on maitrise DNS et la configuration de VHost sous Apache
	*	Et oui le Systeme (SI1, SI5) ça peut servir !
	
	
	N'oublie pas de virer les commentaires sur les instructions importantes (qui ne peuvent être testé sur cette plateforme, et oui je n'ai pas accès à un serveur MySQL sur tech.io 

```php runnable
<?php
//Se connecter au serveur SQL
	$user='root';
	$pass='';
//	$connexion = new PDO('mysql:host=127.0.0.1;dbname=debutterphp', $user, $pass);
	//var_dump($connexion);
	
	//Toujours debugguer sa requete SQL en la plaçant dans une variable
	$sql="SELECT * from profs";
	//var_dump($sql);
	
	//Exécution de la requete et recupération du jeu d'enregistrement (aussi appelé Curseur)
//	$jeu=$connexion->query($sql);
	//var_dump($jeu);
	
?>

<html>

	<table border="1">
		<tr>
			<th>id</th>
			<th>nom</th>
			<th>prenom</th>
		</tr>
		<?php
		//Itération Pour chaque Ligne (Row) du Jeu d'enregistrement($jeu)
		//foreach($jeu as $row){?>
		<tr>
			<td><?php //echo $row["id"] ?></td>
			<td><?php //echo $row["nom"]  ?></td>
			<td><?php //echo $row["prenom"]  ?></td>
		</tr>
		<?php } ?>
	</table>
</html>
?>
```

